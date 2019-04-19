<template>
  <div id="app">
    <div class="wrapper">
      <vue-scroll :ops="ops">
        <dl class="content">
          <dd v-for="i in 20"
              :key="i">
            {{i}}
          </dd>
        </dl>
      </vue-scroll>
    </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Vue from 'vue'
import vuescroll from 'vuescroll'

Vue.use(vuescroll)
export default {
  name: 'App',
  data () {
    return {
      ops: {
        vuescroll: {
          mode: 'slide',
        },
        scrollPanel: {
          scrollingX: false
        }
      }
    }
  },

  components: {
    // HelloWorld
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.wrapper {
  height: 200px;
  width: 100px;
  border: 2px solid black;
  overflow: hidden;
}
.content dd {
  height: 30px;
  width: 100%;
  background: gray;
  margin: 5px 0;
}
</style>
