<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>

    <section class="custom-select">
      <div class="list-items">
        <div class="item" v-for="item in listItem">{{item.title}}</div>
      </div>
      <div class="search">
        <input type="text" name="" value="">
      </div>
    </section>

  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      listItem: [
        {id:1, title:'Option 1', value:'Value1'},
        {id:2, title:'Option 2', value:'Value2'},
        {id:3, title:'Option 3', value:'Value3'},
        {id:4, title:'Option 4', value:'Value4'},
      ]
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

.custom-select {
  position: relative;
  width: 300px;
  margin: 0 auto;
  & input[type="text"] {
    width: 100%;
    height: 40px;
    line-height: 40px;
    display: block;
    padding: 0 6px;
  }
  & .list-items {
    position: absolute;
    top: 45px;
    left: 0;
    width: 100%;
    border: 1px solid green;
  }
}
</style>
