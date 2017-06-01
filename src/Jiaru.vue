<template>
  <div id = "joinPage">
    <joinIntro></joinIntro>
    <joinJob></joinJob>
    <joinTrain></joinTrain>
    <joinWay></joinWay>
    <joinLink></joinLink>
  </div>
</template>

<script>
import joinIntro from './component/join--intro.vue'
import joinJob from './component/join--job.vue'
import joinTrain from './component/join--train.vue'
import joinWay from './component/join--way.vue'
import joinLink from './component/join--link.vue'

export default {
  name: 'joinPage',
  data () {
    return {
      msg: '实验室网站'
    }
  },
  components: { joinIntro, joinJob, joinTrain, joinWay, joinLink }
}
</script>
<style>
.join-container{
  box-sizing: border-box;
  width: 100%;
  min-height: 400px;
  background-size: cover;
  font-size:12px;
  margin-bottom: 45px;
  position: relative;
}
.join--line{
  width: 1px;
  height: 50px;
  background: #ffffff;
  position: absolute;
  content: '';
}
.join--vertical--line{
  transform: rotate(90deg);
}
.join-list ul{
  padding: 0;
  margin: 0 auto;
  margin-top: 45px;
  box-sizing: border-box;
  width: 80%;
  list-style-type: none;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}

</style>
