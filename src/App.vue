<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" v-bind:class="status">Status</h2>
  
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Soldout? Movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array conditional movie</h2>
  
  <h2
    v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      'sold-out' : isSoldOut
    }">Object conditional movie</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Andi",
      channel: "<b>Tutorial Hell</b>",
      headingId:"heading",
      isDisabled: true,
      status: 'danger',
      isPromoted: true,
      isSoldOut: true,
    }
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
</style>
