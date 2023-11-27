<template>
  <section>
    <img v-bind:src="picture" width="210" height="200"/>
    <h1>ชื่อผู้สมัครงาน : {{ getfullName() }}</h1>
    <h1>อายุ : {{ age }} ปี</h1>
    <p>ที่อยู่ : <span v-html="address"></span></p>
    <a :href="social" target="_blank">Facebook</a>
  </section>
</template>
<script>
export default {
  name: 'App',
  data(){
    return{
      firstName:"ศศิธร",
      lastName:"รื่นเจริญ",
      age:16,
      address: "<i>จังหวัดฉะเชิงเทรา</i>",
      picture:"https://cdn-icons-png.flaticon.com/128/11899/11899305.png",
      size:160,
      social:"https://www.facebook.com/profile.php?id=61552541191218"
    }
  },
methods:{
  getfullName(){
    return this.firstName + " "+ this.lastName
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