<template>
  <div id="join--intro" class = 'join-container'>
  	<div class = 'join--intro--text'>
	  <h1>{{ title }}</h1>
	  <p>{{ content }}</p>
	   <div class = "join--line join--vertical--line" id= 'joinIt--line--first'></div>
	  <div class = "join--line" id= 'joinIt--line--second'></div>
	  <div class = "join--line join--vertical--line" id = "joinIt--line--third"></div>
	</div>
  </div>
</template>
 
<script type="text/javascript">
export default {
  data () {
    return {
      title: "交互设计专业介绍",
      content: "你在这里，既可以把握融合新闻的前沿趋势、又可以积累财经新闻的专业素养，既可以掌握公共传播的现代策略、又可以学会数字媒体的先进技术；我们崇尚自由而负责任的传播精神和公共导向，培养你理性、建设性的价值观，和复合型实践、多学科知识、数字化呈现的方法论；我们既重'术'、更重'道'......"
    }
  }
}
</script>

<style>
#join--intro{
	background-image: url('../assets/joinback.png');
	color: #ffffff;
}

#joinIt--line--first{
	top: -15px;
	right: 20px;
}
#joinIt--line--second{
	left: -20px;
	bottom: -20px;
}
#joinIt--line--third{
	bottom: -40px;
}
.join--intro--text{
	position: absolute;
	min-width: 350px;
	max-width: 60%;
	margin-left: 100px;
	margin-right: 100px;
	margin-top: 100px;
}
</style>