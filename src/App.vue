<template>
  <div id="app" class="hello">

    <input type="text" v-model=url />

    <div class="container justify-content-center align-content-center">
      <h1>first qr</h1>
      <QrCode :url=url />
    </div>

  </div>
</template>

<script>
import QrCode from './components/QrCode';

export default {
  name: 'App',
  components: {
    QrCode
  },
  data() {
    return {
      url: ''
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
