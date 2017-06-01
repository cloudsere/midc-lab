<template>
  <div id="join--job" class = 'join-container'>
    <div class = "join--job--intro">
      <div class = "join--line join--vertical--line" id= 'joinJb--line--first'></div>
      <div class = "join--line join--vertical--line" id= 'joinJb--line--second'></div>
      <h2>{{ title }}</h2>
      <p> {{ subtitle }}</p>
      <p> {{ subtitlesm }}</p>
    </div>
      
     <div class = "join-list join--job--choice">
      <ul>
        <li v-for = "choice in jobChoice">
          <img v-bind:src = "choice.jobImage">
          <h3>{{ choice.jobName }}</h3>
          <p>{{ choice.jobIntro }}</p>
          <p>{{ choice.jobIntro }}</p>
        </li>
      </ul>
     </div>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      title: "就业方向",
      subtitle: "交互设计专业融合多学科知识，培养复合型人才",
      subtitlesm: "毕业生有以下就业方向：",
      jobChoice: 
      [
        {jobName:"交互设计师",jobIntro:"介绍内容一句话说明啦啦啦啦啦啦啦",jobImage:"./static/joinjob-choice1.png"},
        {jobName:"前端工程师",jobIntro:"介绍内容一句话说明啦啦啦啦啦啦啦",jobImage:"./static/joinjob-choice2.png"},
        {jobName:"产品经理",jobIntro:"介绍内容一句话说明啦啦啦啦啦啦啦",jobImage:"./static/joinjob-choice3.png"},
        {jobName:"服务设计师",jobIntro:"介绍内容一句话说明啦啦啦啦啦啦啦",jobImage:"./static/joinjob-choice4.png"}
      ]
    }
  }
}

</script>
 
<style>
#join--job{
  text-align:center;
  min-height: 400px;
}
#joinJb--line--first{
  background-color: #000000;
  height: 100px;
  top: -38px;
  left:calc( 50% - 100px );
}
#joinJb--line--second{
  background: #000000;
  height: 100px;
  top: -38px;
  left:calc( 50% + 100px );
}
.join--job--intro h2{
  margin-bottom: 20px;
}
.join--job--choice ul li{
  flex-basis: auto;
}
.join--job--choice ul p{
  font-size: 10px;
}

</style>