<template>
  <div id="join--train" class = 'join-container'>
    <div class = "join--train--intro">
      <div class = "join--line join--vertical--line" id= 'joinTr--line--first'></div>
      <div class = "join--line join--vertical--line" id= 'joinTr--line--second'></div>
      <h2>{{ title }}</h2>
    </div>
      
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      title: "培养方案"
    }
  }
}

</script>
 
<style>
#join--train{
  padding-top: 60px;
  text-align:center;
  background-image: url('../assets/jointrain-back.png');
  color: #ffffff;
}
#joinTr--line--first{
  background: #ffffff;
  height: 100px;
  top: 20px;
  left:calc( 50% - 100px );
}
#joinTr--line--second{
  background: #ffffff;
  height: 100px;
  top: 20px;
  left:calc( 50% + 100px );
}


</style>