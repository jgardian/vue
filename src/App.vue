<template>
  <div id="app">
  
    <h1> Witaj w systemie do zapisow na zajecia</h1>
    <div v-if ="isAuthenticated">
    <h2> Zalogowany jako {{email}}</h2>
   <button @click="toggleAuth()">Wyloguj</button>
    </div>
 <div v-else>
  
   <h2> Zaloguj sie emailem </h2>
    <input type="email" v-model="email">
    <button @click="toggleAuth()">Wchodze</button>
  </div>

 
  </div>
</template>

<script>
import "milligram";
export default {
 data() {
     return {
         email: '',
         isAuthenticated:false
     }
 },
 methods: {
     toggleAuth() {
     this.isAuthenticated =!this.isAuthenticated;
	}
 },
 
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
