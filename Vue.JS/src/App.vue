<template>
  <div id="app">
    <h1> {{ nama }}</h1>
    <h2> Nama: <input v-models="nama"><br></h2>
    <h2> Nilai Anda:&nbsp{{ nilai }}</h2>
    <button @click="totalnilai">Click Me</button>
    <h2>1. Berapakah hasil dari 5 x 5 </h2>
    <input type="radio" v-model="soal1" value="20">20&nbsp&nbsp
    <input type="radio" v-model="soal1" value="25">25&nbsp&nbsp
    <input type="radio" v-model="soal1" value="10">10&nbsp&nbsp
    <input type="radio" v-model="soal1" value="15">15&nbsp&nbsp<br>
    <h2>2. Berapakah titik sudut segitiga</h2>
    <input type="radio" v-model="soal2" value="2">2&nbsp&nbsp
    <input type="radio" v-model="soal2" value="3">3&nbsp&nbsp
    <input type="radio" v-model="soal2" value="4">4&nbsp&nbsp
    <input type="radio" v-model="soal2" value="1">1&nbsp&nbsp<br>
    <h2>3. Ada berapakah jumlah kaki ayam ?</h2>
    <input type="radio" v-model="soal3" value="3">3&nbsp&nbsp
    <input type="radio" v-model="soal3" value="2">2&nbsp&nbsp
    <input type="radio" v-model="soal3" value="1">1&nbsp&nbsp
    <input type="radio" v-model="soal3" value="4">4&nbsp&nbsp<br>
  </div>
</template>

<script>
  
  export default {
    name: 'app',
    data() {
      return{
        nama: '',
        nilai: 0,
        soal1: '',
        soal2: '',
        soal3: ''
      }
    },
    methods:{
      totalnilai(){
        if (this.soal1 == '25' && this.soal2 == '3' && this.soal3 == '2') {
          this.nilai=+3
        }
        else if (this.soal1 == '25' && this.soal2 == '3') {
          this.nilai=+2
        }
        else if (this.soal2 == '3' && this.soal3 == '2') {
          this.nilai=+2
        }
        else if (this.soal1 == '25' && this.soal3 == '2') {
          this.nilai=+2
        }
        else if (this.soal1 == '25') {
          this.nilai=+1
        }
        else if (this.soal2 == '3') {
          this.nilai=+1
        }
        else if (this.soal3 == '2') {
          this.nilai=+1
        }
        else {
          this.nilai = 0
        }
      }
    }
  }
</script>