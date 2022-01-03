<template>
  <div class="consoleComponent">
    <h1 class="title">Console Sounds</h1>
    <div class="consoleBox">
      <button class="consoleButtons" @keydown="playSound($event)">
        Q
        <audio ref="audioApplause" :src="applause"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        W
        <audio ref="audioHorn" :src="horn"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        E
        <audio ref="audioGunShot" :src="gunShot"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        R
        <audio ref="audioLaserShot" :src="laserShot"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        T
        <audio ref="audioHorn" :src="horn"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        Y
        <audio ref="audioHorn" :src="horn"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        U
        <audio ref="audioHorn" :src="horn"></audio>
      </button>

      <button class="consoleButtons" @keydown="playSound($event)">
        I
        <audio ref="audioHorn" :src="horn"></audio>
      </button>
    </div>
  </div>
</template>

<script>
import applause from '../assets/sounds/applause.mp3';
import horn from '../assets/sounds/horn.mp3';
import gunShot from '../assets/sounds/gunShot.mp3';
import laserShot from '../assets/sounds/laserShot.mp3';

export default {
  name: 'HelloWorld',
  data() {
    return {
      applause: applause,
      horn: horn,
      gunShot: gunShot,
      laserShot: laserShot,
    }
  },
  methods: {
    playSound(event) {
      switch(event.key) {
        case 'q': 
        this.$refs.audioApplause.play();
        break;

        case 'w':
        this.$refs.audioHorn.play();
        break;

        case 'e':
        this.$refs.audioGunShot.play();
        break;

        case 'r':
        this.$refs.audioLaserShot.play();
        break;

        case 't':
        this.$refs.audioHorn.play();
        break;

        case 'y':
        this.$refs.audioHorn.play();
        break;

        case 'u':
        this.$refs.audioHorn.play();
        break;

        case 'i':
        this.$refs.audioHorn.play();
        break;
      }
    }
  }
}
</script>

<style scoped>
.consoleComponent {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: linear-gradient(100deg, rgba(185,0,122,1) 0%, rgba(253,187,45,1) 100%);;
}

.title {
  position: absolute;
  top: 5%;
  font-size: 50px;
  color: #fff;
}

.consoleBox {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  flex-wrap: wrap;
  width: 60%;
  height: 40%;
  border: 4px solid #fff;
  border-radius: 10px;
}

.consoleButtons {
  width: 6%;
  height: 20%;
  border: 4px solid #fff;
  border-radius: 10px;
  background: transparent;
  cursor: pointer;
  outline: none;
  color: #fff;
}

.pressed:active {
  background: #fff;
}
</style>
