<template lang="pug">
section#hero
  transition(name="fade")
    PasticheLogo(v-if="loaded")
  transition(name="fade-up")
    .infobox(v-if="loaded")
      p Pastiche GmbH
      p Design &amp; Development Consultancy
      p Zürich, Switzerland
      p 
        a(href="mailto:info@pastiche.io") info@pastiche.io
</template>

<script>
import PasticheLogo from '~/components/PasticheLogo.vue'

export default {
  components: {
    PasticheLogo
  },
  data () {
    return {
      loaded: false
    }
  },
  mounted () {
    this.loaded = true
  }
}
</script>

<style lang="scss" scoped>
#hero {
  height: 100vh;
  padding: 5vw;
}

.logo {
  fill: currentColor;
}

.infobox {
  display: block;
  position: absolute;
  bottom: 5vw;
  right: 5vw;
  line-height: 1.6;
  text-align: right;
  font-weight: 500;

  a {
    color: salmon;
  }
}

.fade-enter-active, .fade-leave-active {
  transition: all 1s;
  filter: none;

}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  filter: blur(10px);
}

.fade-up-enter-active, .fade-up-leave-active {
  transition: transform 1s, opacity 1s cubic-bezier(0.23, 1, 0.32, 1);
}
.fade-up-enter, .fade-up-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(3rem);
}
</style>
