<script>

import TextBind from './components/TextBind.vue';

// vue 사용 선언
export default {
  components : {
    TextBind,
  },
  data(){
    return {
      fruits: ['Apple', 'Banana', 'Orange', 'Apple'],
      user : {
        name : 'junmo',
        age : 26,
        city: 'Dalla',
      }
    }
  }
}
</script>

<template>
  <!-- <ul v-for="(fruit, index) in fruits" :key="index">
    <li>{{index}}{{fruit}}</li>
  </ul> -->
  <ul>
    <template v-for="(value, key, index) in user" :key="index">
      <li>{{index}}, {{key}}, {{value}}</li>
    </template>
  </ul>
  <ul>
    <template v-for="(fruit, index) in fruits" :key="index">
    <li>{{index}}, {{fruit}}</li>
    </template>
  </ul>

</template>

<style>

</style>
