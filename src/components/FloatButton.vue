<template>
  <div class="fixed-action-btn" >
  <a class="btn-floating btn-large red" @click="getCharacter">
    <i class="large material-icons">add</i>
  </a>

</div>
      
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      character: [],
      index: 0
    };
  },
  methods: {
    getCharacter() {
      axios
        .get("https://swapi.co/api/people/" + ++this.index)
        .then(response => {
          // handle success
          console.log(response);

          this.character.push(response.data);

          this.$emit("character-added", this.character);
          console.log(this.character);
        })
        .catch(error => {
          // handle error
          console.log(error);
        })
        .then(() => {
          // always executed
        });
    }
  }
};
</script>

<style>
</style>
