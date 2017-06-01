<template>
  <div id="index--lab" class = 'index--container'>
      <div class = "join--line join--vertical--line" id= 'indexLab--line--first'></div>
      <div class = "join--line join--vertical--line" id= 'indexLab--line--second'></div>
      <h2>{{ title }}</h2>
    

    <div class = 'index--lab--container'>
      <div class = 'index--lab--picture'>
      </div>
      <div class = 'index--lab--des'>
        <p>{{ desFirst }}</p>
        <ul>

          <li>
            <div class = "index--labDes--pic" id="labDes-first"></div>
            <p>{{ jobDes[0] }} </p>
          </li>

          <li>
            <div class = "index--labDes--pic" id="labDes-second"></div>
            <p>{{ jobDes[1] }} </p>
          </li>

          <li>
            <div class = "index--labDes--pic" id="labDes-third"></div>
            <p>{{ jobDes[2] }} </p>
          </li>

        </ul>
         <p>{{ desSecond }}</p>
      </div> 
    </div>

    <div class = 'index--lab--footer'>
    </div>
      
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      title: "实 验 室",
      subtitle: "交互设计专业融合多学科知识，培养复合型人才",
      desFirst:"中山大学媒体交互设计中心成立于2013年，是依托中山大学传播与设计学院建立的，以新媒体设计为基础，以计算机科学为技术手段，以新闻传播学和大数据传播为主要切入点的媒体交互实验室。",
      desSecond:"媒体交互设计中心聚集了来自设计学、计算机科学、视觉文化和用户研究等多个学科领域的成员。",
      jobDes:["UI设计", "编程技术", "用户体验"]
    }
  }
}

</script>
 
<style>
#index--lab{
  text-align:center;
  min-height: 400px;
}
#indexLab--line--first{
  background-color: #000000;
  height: 100px;
  top: -38px;
  left:calc( 50% - 100px );
}
#indexLab--line--second{
  background: #000000;
  height: 100px;
  top: -38px;
  left:calc( 50% + 100px );
}
.index--lab--container{
  display: flex;
  height: 300px;
  justify-content: center;
  margin-top: 30px;
}
.index--lab--picture{
  height: 250px;
  min-width: 250px;
  background-image: url('../assets/index--lab--photo.png');
  background-size:cover;
  margin-right: 30px;
}
.index--lab--des{
  height: 200px;
  width: 280px;
  text-align: left;
  margin-left: 60px;
}
.index--lab--des ul{
  margin-top: 25px;
  margin-bottom: 25px;
  list-style-type: none;
  display: flex;
  justify-content: space-between;
}
.index--lab--des ul li{
  min-width: 80px;
  text-align: center;
}
.index--labDes--pic{
  height: 80px;
  width: 80px;
  background-image: url('../assets/index--labDes--pic.png');
  background-repeat: no-repeat;
  background-color: #edb900;
}
.index--labDes--pic:hover{
  background-color: #444444;
}
#labDes-first{
  background-position: 23px 25px;
}
#labDes-second{
  background-position: -50px 25px;
}
#labDes-third{
  background-position: -125px 25px;
}
.index--lab--footer{
  height: 100px;
  width: 100%;
  background-color: #efefef;
}
</style>