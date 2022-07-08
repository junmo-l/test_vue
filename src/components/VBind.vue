<script>

import TextBind from './TextBind.vue';

// vue 사용 선언
export default {
  components : {
    TextBind,
  },
  data() {
    return {
      bind_url : 'http://www.google.com',
      // bind_url : 'http://www.daum.net',
      bind_a : {
        bind_url : 'http://www.daum.net',
        domain_name : 'daum',
      },
      bind_img :{
        src : 'https://placeimg.com/100/100/any',
        name : 'any',
        // src_name : 'image size 100*100',
      }
    }
  }
}
</script>

<template>
<img src="" alt="">
<img v-bind:src="bind_img.src" alt="bind_img.name">
<a v-bind:href="bind_url">google</a>
<h2 id="title">Hello World !!</h2>
<a v-bind:href="bind_a.bind_url">{{bind_a.domain_name}}</a>
  <!-- <TextBind/> -->
</template>

<style scoped>
#title {
  color : salmon;
  text-align: center;
}
</style>
