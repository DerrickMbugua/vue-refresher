<template>

  <button @click="count++">{{ count }}</button>
  <h2>Hello {{ name }}</h2>
  <h3 v-text="msg"></h3>
  <div v-html="text"></div>
  <div v-bind:id="headingId">Heading</div>
  <button :disabled="isDisabled">Bind</button>
  <p class="underline">Underline</p>
  <p class="underline" v-bind:class="status">Status 2</p>
  <p v-bind:class="isPromoted && 'promoted'">Status 3</p>
  <p :class="isColor ? 'sold-out' : 'new'">Sold out?</p>
  <p :class="['new', 'promoted']">Newly promoted</p>
  <p :class="[isPromoted && 'promoted', isColor ? 'sold-out' : 'new']">Array conditional movie</p>
  <p :class="{
    promoted: isPromoted,
    'sold-out': isColor,
    new: !isColor
  }">Object conditional movie</p>
  <p :style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '10px'
  }">Style Binding</p>

<p :style="headerStyleObject">Object Style Binding</p>
<p :style="[headerStyleObject, headerSpacing]">Array Object Style Binding</p>
</template>

<script>


export default {
 
  data() {
    return {
      count: 0,
      name: "Derrick",
      msg: "Nmeiva",
      text: "<p>Testing</p>",
      headingId: "heading",
      isDisabled: false,
      status: 'danger',
      isPromoted: true,
      isColor: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px'
        
      },
      headerSpacing: {
        padding: '10px'
      }
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
.underline{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}
.new{
  color: blue;
}
.sold-out{
  color: red;
}
</style>
