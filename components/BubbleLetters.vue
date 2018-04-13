<template lang="pug">
  .bubble-letters
    img(v-for="letter, index in letters" :key="index" :src="'img/letters/'+letter.src" :class="letter.class").letter
</template>

<script>
export default {
  data() {
    return {
      letters: [
        {src: '_0004_p.png', class: 'floatOne'},
        {src: '_0005_a.png', class: 'floatTwo'},
        {src: '_0003_s.png', class: 'floatThree'},
        {src: '_0006_t.png', class: 'floatFour'},
        {src: '_0007_i.png', class: 'floatFive'},
        {src: '_0000_c.png', class: 'floatSix'},
        {src: '_0001_h.png', class: 'floatSeven'},
        {src: '_0002_e.png', class: 'floatEight'},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$float-repeat: infinite;

.bubble-letters {
  height: 100%;
  max-height: 100vh;
  width: 100%;
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
  align-items: center;

  .letter {
    height: 10vw;
    will-change: transform;
  }
}

.floatOne {
  animation: floatOne 15s ease-in-out $float-repeat;
}
.floatTwo {
  animation: floatTwo 13s ease-in-out $float-repeat;
}
.floatThree {
  animation: floatThree 14s ease-in-out $float-repeat;
}
.floatFour {
  animation: floatThree 15s ease-in-out $float-repeat;
}
.floatFive {
  animation: floatOne 13s ease-in-out $float-repeat;
}
.floatSix {
  animation: floatTwo 15s ease-in-out $float-repeat;
}
.floatSeven {
  animation: floatThree 12s ease-in-out $float-repeat;
}
.floatEight {
  animation: floatThree 11s ease-in-out $float-repeat;
}

@keyframes floatOne {
      0% {
          transform: none;
      }
      50% {
          transform: translatey(-20px) rotate(5deg);
      }
      100% {
          transform: none;
      }
  }

  @keyframes floatTwo {
      0% {
          transform: none;
      }
      50% {
          transform: translatey(-16px) rotate(-4deg);
      }
      100% {
          transform: none;
      }
  }

  @keyframes floatThree {
      0% {
          transform: none;
      }
      50% {
          transform: translatey(-10px) rotate(2deg);
      }
      100% {
          transform: none;
      }
  }

  @keyframes foatFour {
      0% {
          transform: none;
      }
      25% {
          transform: translatey(-10px) rotate(-2deg);
      }
      75% {
          transform: translatey(5px) rotate(2deg);
      }
      100% {
          transform: none;
      }
  }

</style>
