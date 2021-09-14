<template>
  <div id="app">
    
    <button @click="shuffle">Shuffle</button>
    <transition-group name="cell" tag="div" class="container">
      <my-block v-for="item in items" :key="item" class="cell">{{ item }}</my-block>
    </transition-group>
    <hr>
    <my-block >12311HELLOWORLD</my-block>
  </div>
</template>

<script>
import _ from 'lodash'
import MyBlock from './components/Block'

export default {
  name: "App",
  components: { MyBlock },
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    }
  },
  methods: {
    shuffle() {
      this.items = _.shuffle(this.items)
    },
  },
};
</script>

<style>
.container{
  width: 400px;
}
.cell-move {
  transition: transform 1s;
}
</style>
