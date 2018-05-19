<template>
  <div id="app">
    
    
    <h1> Twoj email to {{email}}</h1>
    
    <div v-if="email.length < 10">Ale masz krotki adres!</div>
<div v-else-if="email.length < 15">Twoj adres e-mail jest w sam raz.</div>
<div v-else>Twój adres e-mail jest stanowczo za d³ugi.</div>
<input type="email" v-model="email">

<button @click="alertMyEmail()">Wyswietl moj e-mail w alercie</button>

    
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      email: ''
      
    }
  },
  methods: {
  alertMyEmail() {
    alert(this.email);
  }
}
  
  
}
</script>


<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
