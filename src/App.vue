<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue"
import Middle from './components/Middle.vue';
import Slot from './components/Slot.vue';

export default {
  components: {
    "Middle": Middle,
    "Header": Header,
    "slot-samp": Slot
  },
  data() {
    return {
      sample: "Harsh",
      ninga:
        [
          { name: "harsh", discription: "the is good ", show: false },
          { name: "muskan", discription: "she is good ", show: false },
          { name: "daksh", discription: "he is good ", show: false },
        ]
    }
  }
}


</script>

<template>

  <h1>{{ sample }}</h1>
  <!-- <Header ></Header> -->
  <!-- <Middle  v-bind:ninga="ninga" ></Middle> -->
  <slot-samp>
    <h1>sample data here</h1>
    <p>Hello how are you </p>
  </slot-samp>
</template>

<style scoped></style>
