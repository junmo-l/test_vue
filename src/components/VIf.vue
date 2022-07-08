<script>

import TextBind from './components/TextBind.vue';
import VBind from './components/VBind.vue';

// vue 사용 선언
export default {
  components: {
    TextBind,
    VBind,
  },
  data() {
    return {
      isActive: false,
      user : {
        name : 'junmo',
        age : 15
      }
    }
  }
}
</script>

<template>
  <!-- <TextBind/> -->
  <!-- <VBind/> -->
  <input type="text" name="" id="" v-model="user.age"> {{user.age}}
  <h2 v-if="user.age > 18">Adult {{user.name}}</h2>
  <h2 v-else-if="user.age > 14">Teenage {{user.name}}</h2>
  <h2 v-else> Child> {{user.name}}</h2>

  <template v-if="isActive">
    <h2>Hello World</h2>
    <hr>
  </template>

  <template v-else>
    <h2>Good Bye</h2>
  </template>

  <!-- <h2 v-if="isActive">Hello World</h2>
  <h2 v-else>Good Bye</h2> -->

</template>

<style>
</style>
