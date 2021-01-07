<template>
  <div class="hello">
    <trading-vue titleTxt="Trading" :data="this.$data"></trading-vue>
  </div>
</template>

<script>
import TradingVue from 'trading-vue-js'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    TradingVue
  },
  mounted() {
    this.run()
  },
  data() {
    return {
      ohlcv: [
        [ 1551128400000, 33,  37.1, 14,  14,  196 ],
        [ 1551132000000, 13.7, 30, 6.6,  30,  206 ],
        [ 1551135600000, 29.9, 33, 21.3, 21.8, 74 ],
        [ 1551139200000, 21.7, 25.9, 18, 24,  140 ],
        [ 1551142800000, 24.1, 24.1, 24, 24.1, 29 ],
      ]
    }
  },
  methods: {
    run() {
      var self = this
      setInterval(function (){
        console.log('cuong')
        let  a = 24.1;
        let  b = 24.1;
        let  c = 24;
        let  d = 24.1;
        let  e = 29;
        let latsIndex = self.ohlcv[self.ohlcv.length - 1][0]
        console.log(latsIndex)
        console.log(self.ohlcv.length)
        self.ohlcv.push([latsIndex + 1000000, a, b, c, d ,e])
      }, 2000)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
