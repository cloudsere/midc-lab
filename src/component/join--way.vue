<template>
  <div id="join--way" class = 'join-container'>
    <div class = "join--way--intro">
      <h2>{{ title }}</h2>
      <div class = "join--line join--vertical--line" id= 'joinWay--line--first'></div>
    </div>
     
    <div class = "join-list join--way--choice">
      <ul>
        <li v-for = "choice in way">
          <div class = "join--way--choice--content">
            <img :src = "choice.image">
            <h3>{{ choice.name }}</h3>
            <p>{{ choice.intro }}</p>
          </div>
          <h3>{{ choice.time }}</h3>
        </li>
      </ul>
     </div> 
     
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      title: "加入途径",
      way:[
      {name: "保研夏令营",intro:"学生可根据学院要求提交申请材料，经过选拔后参加夏令营活动，获取保研资格",time:"每年7月",image:"./static/joinway--choice1.png"},
      {name: "保送研究生面试",intro:"学生可根据学院要求提交申请材料，经过选拔后参加夏令营活动，获取保研资格",time:"每年7月",image:"./static/joinway--choice2.png"},
      {name: "统考研究生考试",intro:"学生可根据学院要求提交申请材料，经过选拔后参加夏令营活动，获取保研资格",time:"每年7月",image:"./static/joinway--choice3.png"}
      ]
    }
  }
}

</script>
 
<style>
#join--way{
  padding-top: 60px;
  padding-bottom: 60px;
  text-align:center;
  background-color: #efefef;
}
#joinWay--line--first{
  background: #000000;
  top: 90px;
  left: 50%;
}
.join--way--choice li{
  max-width: 190px;
}
.join--way--choice--content{
  height: 220px;
  padding:20px;
  background: #ffffff;
  margin-top: 30px;
  margin-bottom: 30px;
}

.join--way--choice--content:after{
    content: '';
    width: 0;
    height: 0;
    border-top: solid 50px #ffffff;
    border-left: solid 50px transparent;
    border-right: solid 50px transparent;
    position:relative;
    top: 70px;
}
.join--way--choice--content:hover{
  background: #f2c125;
  color: #ffffff;
}
.join--way--choice--content:hover:after{
    content: '';
    width: 0;
    height: 0;
    border-top: solid 50px #f2c125;
    border-left: solid 50px transparent;
    border-right: solid 50px transparent;
    position:relative;
    top: 70px;
}
.join--way--choice--content:hover img{
  filter: brightness(0) invert(1);
}
</style>