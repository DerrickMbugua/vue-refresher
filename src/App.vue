<template>
<h1 :style="headerStyling">List Rendering</h1>
<p v-for="(customer, index) in customers" :key="customer">{{ index + 1 }} {{ customer }}</p>
<p v-for="item in clients" :key="item.name">{{ item.name }} {{ item.department }}</p>
<template v-for="dev in developers" :key="dev">
  <p>{{ dev.name }}</p>
  <p v-for="lang in dev.languages" :key="lang">{{ lang }}</p>
</template>
<p v-for="detail in myInfo" :key="detail">{{ detail }}</p>
</template>

<script>


export default {
 
  data() {
    return {
      headerStyling: {
        color: 'blue',
        fontSize: '30px',
        padding: '5px'
      },
      customers: ['Bruce', 'Jane', 'James', 'Mary'],
      clients: [
        {name: 'Derrick', department: 'G'},
        {name: 'Mbugua', department: 'G'},
        {name: 'Mwema', department: 'G'},
        {name: 'Sam', department: 'G'},
      ],
      developers: [
        {
          name: 'Sparta',
          languages: ['php','css']
        },
        {
          name: 'Meg',
          languages: ['node', 'flutter']
        }
      ],
      myInfo: {
        name: 'D Mwema',
        channel: 'dev',
        language: 'Vue 3'
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

</style>
