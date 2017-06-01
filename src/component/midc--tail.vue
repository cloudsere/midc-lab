<template>
	<div>
		<div id='midc--info'>
			<img class='bg_img' v-bind:src=midc_map>
			<!--<img class='float_img' v-bind:src=midc_cont> -->
		</div>

		<div id='midc--bottom'>
			<p>{{copyright}}</p>
		</div>
	</div>

</template>

<script>
export default {
  data() {
    return {
    	midc_map: './static/bottom_info.png',
    	//midc_cont: "./static/bottom_contact.png"
    	copyright: 'COPYRIGHT©2015 中山大学传播与设计学院 媒体交互设计中心'
    }
  }
}
</script>

<style>

#midc--info{
	height: 372px;
	text-align: center;
}

#midc--bottom{
	text-align: center;
	width: 100%;
	height: 40px;
	background-color: #333333;
}

#midc--bottom p{
	margin:0 auto; 
	font-size: 14px;
	color: white;
	line-height: 40px;
	font: 'Microsoft YaHei';
}

</style>