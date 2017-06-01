<template>
  <div>
      <ul class="works--tab">
        <li v-for = "name in tabName" class="works-tab-item"> 
          <p> {{ name }}</p>
        </li>
      </ul>
      <div class = >
      </div>
  </div>
</template>

<script>
import joinIntro from './component/join--intro.vue'

export default {
  name: 'joinPage',
  data () {
    return {
      msg: '实验室网站',
      tabName: ['交互设计','服务设计','可视化设计']
    }
  },
  components: { joinIntro }
}
</script>
<style>

</style>
