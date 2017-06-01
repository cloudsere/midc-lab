<template>
  <div id='midc--lab'>
    <div id='midc--tcontainer'>
      <img id='midc--logo' v-bind:src = "midc_logo">
      <ul>
       
        <li>
          <router-link to = '/second'>
            <p>{{ midc_tab[3] }}</p>
          </router-link>
        </li>

        <li>
          <router-link to = '/third'>
            <p>{{ midc_tab[2] }}</p>
          </router-link>
        </li>

        <li>
          <router-link to = '/second'>
            <p>{{ midc_tab[1] }}</p>
          </router-link>
        </li>

        <li>
          <router-link to = '/first'>
            <p>{{ midc_tab[0] }}</p>
          </router-link>
        </li>
      </ul>
    </div>
    <router-view class= "view"></router-view>
    <div class = 'midc--footer--bar'>
      <p> {{ footer }} </p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      midc_logo: "./static/header_logo.png",
      midc_tab: ['首页','我们','作品','加入'],
      footer:"COPYRIGHT©2015  中山大学传播与设计学院  媒体交互设计中心"
    }
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  font-family: 'Microsoft YaHei';
}
#midc--logo{
  margin-left: 60px;
}
#midc--tcontainer{
  height: 60px;
  width: 100%;
  background-color: #444444;
  overflow:hidden;
}

#midc--tcontainer ul{
  list-style-type: none;
  width: calc( 100% - 300px);
  float: right;
}

#midc--tcontainer ul li{
  float: right;
  width: 100px;
}
#midc--tcontainer ul li a{
  display: block;
  color: #ffffff;
  text-align: center;
  text-decoration: none;
  padding: 24px 16px;
  font-size: 14px;
}
#midc--tcontainer ul li a:hover{
  background-color: #edb900;
}
.midc--footer--bar{
  position: relative;
  bottom: 0;
  width: 100%;
  height: 30px;
  background-color: #444444;
  color: #ffffff;
  text-align: center;
  font-size: 10px;
  line-height: 30px;
}
</style>