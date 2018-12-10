<template lang="pug">
section#hero
  PasticheLogo
  .infobox
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
</style>
