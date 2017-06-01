<template>
  <div>
     <div class = "index--works--title">
      <div class = "join--line join--vertical--line" id= 'indexWk--line--first'></div>
      <div class = "join--line join--vertical--line" id= 'indexWk--line--second'></div>
      <h2>{{ title }}</h2>
    </div>

    <div class = "index--works--header">
      <div class = "index--works--yellow--bar" >
      </div>
    </div>

    <div>
      <ul class = "index--works--list">
        <li v-for = "work in works" class = "works--list--item index-works--list--item">
          <div class = "works--item--img" :style = "{backgroundImage: 'url(' +  work.pic  + ')'}">
          </div>

          <div class = "works--item--title">
            <p>{{ work.title }} </p>
          </div>

          <div class = "works--item--author">
            <p>{{ work.author }} </p>
          </div>

          <div class = "works--item--like" :style = "{backgroundImage: 'url(' +  iconlike  + ')'}">
            <p>{{ work.like }} </p>
          </div>

          <div class = "works--item--open" :style = "{backgroundImage: 'url(' +  iconopen  + ')'}">
            <p>{{ work.open }} </p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: 'joinPage',
  data () {
    return {
      msg: '实验室网站',
      title: '作  品',
      tabName: ['交互设计','服务设计','可视化设计'],
      iconopen: require('../assets/icon--see.png'),
      iconlike: require('../assets/icon--like.png'),
      works: [
      {"title":"作品名称作品名","author":"作者名","open":100,"like":6,"type":"交互设计","pic":require("../assets/works--item--001.png")},
      {"title":"作品名称作品名","author":"作者名","open":100,"like":6,"type":"交互设计","pic":require("../assets/works--item--002.png")},
      {"title":"作品名称作品名","author":"作者名","open":100,"like":6,"type":"交互设计","pic":require("../assets/works--item--003.png")},
      {"title":"作品名称作品名","author":"作者名","open":100,"like":6,"type":"服务设计","pic":require("../assets/works--item--004.png")}
      ]
    }
  }
}
</script>
<style>
.index--works--header{
  height: 150px;
  width: 100%;
  background-color: #3c3c3c;
  box-sizing: border-box;
  padding-top: 40px;
  margin-top: -70px;
}
.index--works--yellow--bar{
  height: 80px;
  width: 70%;
  margin: 0 auto;
  background-color: #efc100;
  content: '';
}
.works--tab{
  padding: 0;
  margin: 0;
  list-style-type: none;
  width: 400px;
  margin: 0 auto;
  text-align: center;
}
.works--tab--item{
  display: inline-block;
  margin: 20px;
}
.works--tab--item p{
  font-size: 12px;
  color: #ffffff;
}
.index--works--list{
  margin: 0 auto;
  width: 70%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  list-style-type: none;
  margin-top: -80px;
}
.index-works--list--item{
  box-sizing: border-box;
  min-width: 200px;
  padding: 15px;
  margin: 20px;
  min-height: 250px;
  background-color: #ffffff;
  color:#969696;
  box-shadow: 0px 7px 10px 3px #b6b6b6;
}
.works--list--item p{
  font-size: 11px;
}
.works--item--img{
  width: 100%;
  height: 85%;
  margin-bottom: 5px;
  background-repeat: no-repeat;
  background-size: cover;
}
.works--item--author{
  float: left;
}
.works--item--open,.works--item--like{
  text-align: right;
  float: right;
  width: 30px;
  background-repeat: no-repeat;
  background-position: 10px 1px;
}
.works--item--open{
  width: 35px;
  background-position: 0px 0px;
}
.index--works--title{
  text-align: center;
  color: #ffffff;
  font-size: 12px;
  position: relative;
}
#indexWk--line--first{
  background: #ffffff;
  height: 100px;
  left:calc( 50% + 100px );
  top: -35px;
}

#indexWk--line--second{
  background: #ffffff;
  height: 100px;
  left:calc( 50% - 100px );
  top: -35px;
}
</style>
