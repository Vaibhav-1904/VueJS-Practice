<template>
      
    <div>

      <h1>{{description}}</h1>

      <br>

      <img src="./assets/gfg.png" alt="" @load="onImageLoad">


    </div>
  
</template>

<script>

export default {
  name:'App',
  
  data() {
    return {
      isImageLoaded: false
    }
  },
  methods: {
    onImageLoad () {
      this.isImageLoaded = true
    }
  },
  watch: {
    isImageLoaded: function(newValue, oldValue) {
      console.log("New value is: " + newValue)
      console.log("Old value is: " + oldValue)
    }
  }
};

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
