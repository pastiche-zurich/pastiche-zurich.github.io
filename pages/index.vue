<template lang="pug">
section#hero
  BubbleLetters
  .infobox
    p Interactive Design &amp; Development
    p Zürich, Switzerland
    p 
      a(href="mailto:info@pastiche.io") info@pastiche.io
</template>

<script>
import BubbleLetters from '~/components/BubbleLetters.vue'

export default {
  components: {
    BubbleLetters
  }
}
</script>

<style lang="scss" scoped>
#hero {
  height: 100vh;
}
.infobox {
  display: block;
  position: absolute;
  bottom: 2rem;
  right: 2rem;
  color: #3c485e;
  letter-spacing: .02rem;
  line-height: 1.6;
  font-weight: 300;
  text-align: right;

  a {
    color: #3c485e;
  }
}
</style>
