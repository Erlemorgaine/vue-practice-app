<template>
  <p :title="hoverText">{{ hoverInstruction }}</p>
  <p v-if="showIfText">{{ifText}}</p>
  <button @click="toggleIfText">{{ btnText }}</button>
</template>

<script>
export default {
  data() {
      return {
        hoverText: 'Show this text on hover',
        hoverInstruction: 'Hover this',
        showIfText: true,
        ifText: 'This text is shown conditionally',
        btnText: 'Toggle text'
      }
  },
  methods:{
    toggleIfText() {
      this.showIfText = !this.showIfText
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

</style>
