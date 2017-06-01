<template>
  <div id="allmap" v-bind:style="mapStyle"></div>
</template>

<script>
export default{
  data:function(){
    return{
      mapStyle:{
        width:'100%',
        height:'200px'
      }
    }
  },
  created(){
    this.loadMap()
  },
  mounted(){
    this.ready();
    this.createMarker()
  },
  methods:{
    loadMap: function(){

    },
    ready: function(){
      var map = new BMap.Map('allmap');
      var point = new BMap.Point(113.394178,23.0711);//定义一个中心点坐标
      map.centerAndZoom(point,17);//设定地图的中心点和坐标并将地图显示在地图容器中
      window.map = map;
    },
    createMarker: function(){
        //创建InfoWindow
      function createInfoWindow(i){
          var json = markerArr[i];
          var iw = new BMap.InfoWindow("<b class='iw_poi_title' title='" + json.title + "'>" + json.title + "</b><div class='iw_poi_content'>"+json.content+"</div>");
          return iw;
      }
        //创建一个Icon
      function createIcon(json){
          var icon = new BMap.Icon("src/assets/map--marker.png", new BMap.Size(json.w,json.h),{imageOffset: new BMap.Size(-json.l,-json.t),infoWindowOffset:new BMap.Size(json.lb+5,1),offset:new BMap.Size(json.x,json.h)})
          return icon;
      }
      var markerArr = [{title:" ",content:" ",point:"113.394151|23.071266",isOpen:0,icon:{w:23,h:25,l:46,t:21,x:9,lb:12}}
         ];
       for(var i=0;i<markerArr.length;i++){
            var json = markerArr[i];
            var p0 = json.point.split("|")[0];
            var p1 = json.point.split("|")[1];
            var point = new BMap.Point(p0,p1);
            var iconImg = createIcon(json.icon);
            var marker = new BMap.Marker(point,{icon:iconImg});
            var iw = createInfoWindow(i);
            var label = new BMap.Label(json.title,{"offset":new BMap.Size(json.icon.lb-json.icon.x+10,-20)});
            marker.setLabel(label);
            map.addOverlay(marker);
            label.setStyle({
                        borderColor:"#808080",
                        color:"#333",
                        cursor:"pointer"
            });
            
            (function(){
                var index = i;
                var _iw = createInfoWindow(i);
                var _marker = marker;
                _marker.addEventListener("click",function(){
                    this.openInfoWindow(_iw);
                });
                _iw.addEventListener("open",function(){
                    _marker.getLabel().hide();
                })
                _iw.addEventListener("close",function(){
                    _marker.getLabel().show();
                })
                label.addEventListener("click",function(){
                    _marker.openInfoWindow(_iw);
                })
                if(!!json.isOpen){
                    label.hide();
                    _marker.openInfoWindow(_iw);
                }
            })()
        }
    }
  }
}
</script>
<!--Add"scoped" attribute to limit CSS to this component only -->
<style>
  #allmap{
    margin-top: 50px;
  }
 .anchorBL {  
    display:none  
  }  
</style>