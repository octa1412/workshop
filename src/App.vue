<template>
  <div id="app">
  <navbar-starwars></navbar-starwars>
  
  <div class="container">
   <character-list :characters="characters"></character-list>
  </div>
  <float-button @character-added= "showCharacter"></float-button>
  </div>
</template>

<script>
import navbarStarwars from "./components/navBarStarwars";
import FloatButton from "./components/FloatButton";
import CharacterList from "./components/CharacterList";

export default {
  name: "App",
  components: {
    navbarStarwars,
    FloatButton,
    CharacterList
  },

  data() {
    return{
      characters: []
    }
  },

  methods:{
    showCharacter(payload) {
      this.characters = payload;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  height: 100vh;
  background-color: white;
  position: relative;
}
</style>
