<template>
  <div id="app" class="app">
    <h1 v-bind:class="{ warning: total >= 3 }">{{ total }}</h1>
    <div v-on:click="increment" class="btn">button</div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      total: 0
    }
  },
  methods: {
    increment: function () {
      this.total++;
    }
  }
}
</script>

<style>
.app {
  padding: 0 25px;
}

.warning {
  color: red;
  font-weight: bold;
}
</style>
