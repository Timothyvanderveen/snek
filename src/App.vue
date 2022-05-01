<template>
  <a target="_blank" href="https://ads.google.com/intl/nl_nl/getstarted/?subid=nl-nl-ha-aw-bk-c-bau!o3~Cj0KCQjwvLOTBhCJARIsACVldV2XIvLagtKhZLsFhT3fGHi4QQc22Bv18iXgLjhIVtwhO8YSQ2N9_LkaAk4YEALw_wcB~105988451885~kwd-12340363~10963318692~459889487207&utm_source=aw&utm_medium=ha&utm_campaign=nl-nl-ha-aw-bk-c-bau!o3~Cj0KCQjwvLOTBhCJARIsACVldV2XIvLagtKhZLsFhT3fGHi4QQc22Bv18iXgLjhIVtwhO8YSQ2N9_LkaAk4YEALw_wcB~105988451885~kwd-12340363~10963318692~459889487207&gclid=Cj0KCQjwvLOTBhCJARIsACVldV2XIvLagtKhZLsFhT3fGHi4QQc22Bv18iXgLjhIVtwhO8YSQ2N9_LkaAk4YEALw_wcB&gclsrc=aw.ds">adwords</a>
    <h1 class="header">crazy frog moment!</h1>

  <img ref="frog1" class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" draggable="true" />
  <img ref="frog2" class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif"  draggable="true"/>
  <img ref="frog3" class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" draggable="true" />
  <br>
    <div @click="right">right</div>
    <div @click="buyBoter">buy boter</div>
    <div @click="levelup">level up!</div>
  <div>Dit is mijn level: {{level}}</div>
  <img @click="eat" class="mouth" src="https://media.istockphoto.com/photos/female-wearing-red-lipstick-with-mouth-open-picture-id465177483?k=20&m=465177483&s=612x612&w=0&h=N-KHb1UIWpjxGcpOnGOF1UOOymchH941X670nKcKBHY=" />
  <div @click="eat" class="eating-frog">
  <img style="z-index: 999; position: relative" ref="upper-lip" src="data:image/jpeg;base64,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">
    {{iAte}}
  <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" draggable="true" />
    <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif"  draggable="true"/>
    <img class="frog" src="https://c.tenor.com/E8GnznijhxgAAAAC/frog-dancing.gif" draggable="true" />
  <img ref="downie-lip" src="data:image/jpeg;base64,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">
  </div>

  <img @click="unopacitybat" :style="{opacity }" ref="bat" class="bat" src="https://img.buzzfeed.com/buzzfeed-static/static/2016-07/19/22/enhanced/buzzfeed-prod-fastlane02/enhanced-3551-1468981926-12.jpg" />
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
    level: 1,
    iAte: '',
    opacity: 1,
  }),
  mounted() {
  },
  methods: {
    eat() {
      this.$refs["upper-lip"].animate([
        {transform: "translateY(0)"},
        {transform: "translateY(300px)"},
        {transform: "translateY(0)"},
      ], {
        duration: 1,
        iterations: Infinity
      })
      this.$refs["downie-lip"].animate([
        {transform: "translateY(0)"},
        {transform: "translateY(-320px)"},
        {transform: "translateY(0)"},
      ], {
        duration: 12,
        iterations: Infinity
      })


      const audio = new Audio('https://audio-previews.elements.envatousercontent.com/files/274040460/preview.mp3?response-content-disposition=attachment%3B+filename%3D%22PVPA2XP-eating.mp3%22')
      audio.play()
      this.level = this.level + this.level

      setInterval(() => {
        const audio = new Audio('https://audio-previews.elements.envatousercontent.com/files/274040460/preview.mp3?response-content-disposition=attachment%3B+filename%3D%22PVPA2XP-eating.mp3%22')
        audio.play()
        this.level = this.level + this.level
      }, 1000)

      this.iAte = "YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM YAM "
    },
    right() {
      this.$refs.snek.style.left = "60px";
    },
    unopacitybat() {
      setInterval(() => {
        this.opacity = this.opacity - 0.01
      }, 200)
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
    transform: scaleX(1);
    transform: scaleY(2);
  }
  50% {
    filter: grayscale(1) sepia(0);
    transform: scale(1.1);
    transform: scaleY(0.7);
    transform: scaleX(0.7);
  }
  100% {
    filter: grayscale(0) sepia(1);
    transform: scale(1);
    transform: scaleY(.5);
  }
}

* {
  font-family: "Comic Sans MS";
  font-size: 50px;
  color: greenyellow;
}

.eating-frog {
  width: 1px;
}
</style>
