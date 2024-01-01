<template>
  <div class="container">
    <div class="image-container">
      <img id="speech_bubble" alt="Speech_bubble" src="./assets/speech_bubble.png">
      <div class="overlay-text">
        <quote_generator msg="Welcome to quote_generator"/>
      </div>
    </div>
    <img id="cat" alt="Cat" src="./assets/cat.png">
  </div>
  <footer_component/>
</template>

<script>
import quote_generator from './components/quote_generator.vue'
import footer_component from './components/footer.vue'

export default {
  name: 'App',
  components: {
    quote_generator,
    footer_component
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
  background-image: url('./assets/cool-background.png');
  position: fixed;
  min-width: 2200px;
  height: auto;

}

.container {
  position: relative;
  display: inline-block;
}

.speech-bubble {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
}

#speech_bubble {
  width: 500px;
  height: auto; 
  margin-right: 300px;
}

#cat {
  margin-top: 250px;
  min-width: 300px;
  margin-right: 600px;
}

.image-container {
  position: absolute; 
  left: 75%;
  transform: translateX(-50%);
}

.overlay-text {
  top: 20px;
  left: 20px;
  right: 20px;
  bottom: 20px;

  position: fixed;
  display: flex;
  justify-content: center;

  color: #2c3e50;
  font-size: 20px;
  text-align: center;
  vertical-align: top;

  width: 450px;
  height: 200px;
}
</style>