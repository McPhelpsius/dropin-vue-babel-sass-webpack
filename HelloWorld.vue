<template>
  <div class="some-globally-inherited-style">
    <h1>{{title}}</h1>
    <p :style="{color: welcomeMessageColor}">
      {{ welcomeMessage }}
    </p>
    <hr>
    Welcome Message:
    <input type="text" v-model="welcomeMessage">
    <br>
    Color:
    <input type="text" v-model="welcomeMessageColor">
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'Hello World.',
      welcomeMessage: 'Welcome to Vue',
      welcomeMessageColor: this.initialWelcomeMessageColor,
    }
  },
  props: {
    initialWelcomeMessageColor: {
      type: String,
      default: '',
    }
  },
  created() {},
  methods: {
    customConsoleLog(message) {
      console.log(`${Date.now()} ${message}`);
    }
  }
};
</script>
<style lang="scss" scoped>
  h3 { color: green; }
</style>


