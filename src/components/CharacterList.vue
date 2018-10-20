<template>
   <ul class="collection">
    <li class="collection-item avatar" v-for="(character,index) in characters" :key="index">
      <img src="https://us.123rf.com/450wm/solargaria/solargaria1709/solargaria170900008/85425363-user-icon-male-with-beard-icon-hipster-flat-icon-avatar-of-man-with-beard-flat-internet-icon-in-roun.jpg?ver=6" alt="" class="circle">
      <span class="title">{{character.name}}</span>
    </li>
   </ul>
</template>

<script>
export default {
  props: {
    characters: Array
  }
};
</script>

<style>
.collection {
  border: none;
}
</style>
