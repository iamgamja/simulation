<template>
  <div class="main">
    <div class="left">
      <canvas></canvas>
    </div>
    <div class="right">
      <Setting-component v-for="i in 5" v-bind:key="i"></Setting-component>
    </div>
  </div>
</template>

<script>
  import SettingComponent from './components/Setting-component.vue'

  export default {
    name: 'App',
    data() {
      return {

      }
    },
    methods: {

    },
    components: {
      SettingComponent
    }
  }
</script>

<style scoped>
  /* Desktop */
  .main {
    display: flex;
    flex-direction: row;
    height: 100%;
    background: #edf4ff;
  }

  div.left {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100vh;
    height: 100%;
  }

  div.left > canvas {
    background: white;
    border: 1px black solid;
  }

  div.right {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex: 1;
    height: 100%;
    background: #bfd3f3;
  }

  /* Mobile */
  @media ( max-aspect-ratio: 1/1 ) {
    .main {
      flex-direction: column;
    }

    div.left {
      width: initial;
      height: 100vw;
    }
  }
</style>
