<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>{{ judul }}</h2>
    <input v-model="msg"><br>
    <button @click="gantijudul">Ganti Judul</button>
    <br><br>
    <input v-model = "x" type="" name="">
    <h1 v-if= "x % 2 === 0"> Ini adalah bilangan Genap</h1>
    <h1 v-else> Ini adalah bilangan Ganjil</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return{
      msg: 'Renaldy SY',
      judul: 'renaldyy',
      x: 2
    }
  },
mounted() {
  this.judul = "Renaldy SY"
},
methods: {
  gantijudul(){
    this.judul = 'renaldyy'
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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