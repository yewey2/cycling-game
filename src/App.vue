<template>
  <div class="app-container">
    <div class="game-window">
      <br>
      Hello World!
      <Biker />
      <Obstacle />
    </div>
    <div class="controls">
      <button class="btn btn-left" type="button" @click="leftButton"></button>
      <button class="btn btn-right" type="button" @click="rightButton"></button>
    </div>
  </div>
</template>

<script>
import Biker from './components/biker'
import Obstacle from './components/obstacle'

export default {
  name: 'App',
  components: {
    Biker,
    Obstacle
  },
  data() {

  },
  methods: {
    leftButton(){
      console.log('left')
    },
    rightButton(){
      console.log('right')
    },
  },
}
</script>

<style lang="scss">
.app-container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: skyblue;
  margin-inline: auto;
  width: clamp(0px, 600px, 100vw);
  height: 100vh;
  position: relative;
  .controls {
    height: clamp(20vh, 300px, 300px);
    width: 100%;
    background: #ddf;
    position: absolute;
    bottom: 0;
    .btn {
      width: 4rem;
      height: 4rem;
      border-radius: 2rem;
      border: 1px solid #197b96;
      background: #c0a5ae;
      &#{&}-left {
        margin-right: 3rem;
        background: blue;
      }
      &#{&}-left {
        margin-right: 6rem;
        background: green;
      }
    }
  }
}
</style>
