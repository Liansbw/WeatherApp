<template>
  <div id="app">
 
  </div>
</template>

<script>
import axios from "axios"
export default{
  name: "App"
  data() {
    return {
      APIkey "6f2e71f43aa54f01a14730a91198aa67",
      city: "Detroit",
    };
    created(){
      this.getCurrentWeather()
    }
  }
  methods: {
    getCurrentWeather() {
      axios.get ("https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&appid={API key}"
      ).then(res => {
        console.log(res.data)
      ;
      )
      });

    }
  }
}
</script>

<style lang="scss">
{
  margin: 0;
  padding: 0;
  box-sizing: border box;
  font-family: "Quicksand"

}
</style>
