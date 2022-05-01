<template>
    <div @click="right">right</div>
    <div @click="buyBoter">buy boter</div>
    <div @click="levelup">level up!</div>
  <div>Dit is mijn level: {{level}}</div>
  <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" />
  <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" />
  <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" />
  <img class="frog" src="https://img.buzzfeed.com/buzzfeed-static/static/2016-07/19/22/enhanced/buzzfeed-prod-fastlane02/enhanced-3551-1468981926-12.jpg" />
    <div class="container">
      <div class="snek" ref="snek"></div>
      <div class="apple" ref="apple"></div>
      <div :key="item" v-for="item in [1,2,3,4]">
        <div v-if="item % 2 === 0" class="black"></div>
        <div v-else class="white"></div>
      </div>
      <div :key="item" v-for="item in [1,2,3,4]">
        <div v-if="item % 2 === 1" class="black"></div>
        <div v-else class="white"></div>
      </div>
      <div :key="item" v-for="item in [1,2,3,4]">
        <div v-if="item % 2 === 0" class="black"></div>
        <div v-else class="white"></div>
      </div>
      <div :key="item" v-for="item in [1,2,3,4]">
        <div v-if="item % 2 === 1" class="black"></div>
        <div v-else class="white"></div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    level: 1
  }),
  mounted() {
  },
  methods: {
    right() {
      this.$refs.snek.style.left = "60px";
    },
    buyBoter() {
      this.$refs.snek.innerHTML = 'wow u bought boter'
    },
    levelup() {
      this.$refs.apple.innerHTML = 'dingdingding you are now level 4'

      const audio = new Audio('https://www.intonaija.com/dwl/music/Crazy_Frog_-_Axel_F_Soloplay.ng_.mp3')
      audio.play()
      this.level = this.level + this.level

      setInterval(() => {
        const audio = new Audio('https://www.intonaija.com/dwl/music/Crazy_Frog_-_Axel_F_Soloplay.ng_.mp3')
        audio.play()
        this.level = this.level + this.level
      }, 10000)

      this.$refs.apple.animate([
        {transform: 'translate(12px, 234px)'},
        {transform: 'translateY(2px, 123px)'},
        {transform: 'translate(12px, 234px)'},
        {transform: 'translateY(2px, 123px)'},
      ], {
        duration: 1,
        iterations: Infinity
      })
    },
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

.snek {
  width: 30px;
  position: absolute;
  height: 30px;
  background: greenyellow;
  margin: 10px;
  left: 10px;
  transition: left 1s;
}

.apple {
  background: yellow;
  width: 30px;
  position: absolute;
  height: 30px;
top: 180px;
  left: 10px;
  margin: 10px;
}


.container {
  width: 200px;
  display: flex;
  flex-wrap: wrap;
}

.black {
  width: 50px;
  height: 50px;
  background: black;
}

.white {
  width: 50px;
  height: 50px;
  background: red;
}

.frog {
  filter: grayscale(1) sepia(1);
  animation: frog .5s infinite;
}

@keyframes frog {
  0% {
    filter: grayscale(0) sepia(1);
  }
  50% {
    filter: grayscale(1) sepia(0);
  }
  100% {
    filter: grayscale(0) sepia(1);
  }
}
</style>
