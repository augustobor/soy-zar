<template>
  <router-view/>
</template>
<script>

export default {
  name: 'App',
}
</script>
<style>
* {
  margin: 0;
  padding: 0;  
  
  box-sizing: border-box;
  text-align: center;
}

html {
	font-size: 62.5%;
	font-family: 'Arvo', serif;
	scroll-behavior: smooth;
}

#app {
  width: 100vw;
  height: 100vh;
}
</style>
