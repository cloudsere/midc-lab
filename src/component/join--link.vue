<template>
  <div id="join--link" class = 'join-container'>
    <div class = "join--link--intro">
      <h1>{{ title }}</h1>
      <div class = "join--line join--vertical--line" id= 'joinLink--line--first'></div>
    </div>
     
    <div class = "join-list join--link--choice">
      <ul>
        <li v-for = "choice in link">
          <div class = "join--link--choice--content">
            
            <img v-bind:src = "choice.image">
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
      title: "相关链接",
      link:[
      {name: "中山大学官网",image:"./static/join--link--school.png"},
      {name: "中山大学传播与设计学院",image:"./static/join--link--school.png"},
      {name: "中山大学研究生院",image:"./static/join--link--school.png"},
      {name: "中山大学校务部",image:"./static/join--link--school.png"}
      ]
    }
  }
}

</script>
 
<style>
#join--link{
  padding-top: 60px;
  text-align:center;
  background-color: #ffffff;
  min-height: 300px;
  color: #363636;
  font-size: 10px;
}
#joinLink--line--first{
  background: #000000;
  top: 30%;
  left: 50%;
}
.join--link--choice li{
  box-sizing: border-box;
  padding: 20px;
  max-width: 200px;
  height: 120px;
  border-top: 1px solid #363636;
  border-bottom: 1px solid #363636;
}
.join--link--choice li:hover{
  box-sizing: border-box;
  border-left: 1px solid #363636;
  border-right: 1px solid #363636;
}
.join--link--choice ul{
  margin-top:100px;
}
.join--link--choice--content{
  height: 220px;
}



</style>