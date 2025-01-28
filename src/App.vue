<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue"
import Middle from './components/Middle.vue';
import Slot from './components/Slot.vue';
import AddBlog from './components/AddBlog.vue';
import GetAllBlogs from './components/GetAllBlogs.vue';

export default {
  components: {
    Middle,
    "Header": Header,
    "slot-samp": Slot,
    AddBlog,
  GetAllBlogs,
  },
  data() {
    return {
      sample: "Middle",
      ninga:
        [
          { name: "monti", discription: "the is good ", show: false },
          { name: "bunti", discription: "she is good ", show: false },
          { name: "shonti", discription: "he is good ", show: false },
        ]
    }
  }
}


</script>

<template>

  <!-- <h1>{{ sample }}</h1> -->
  <!-- <Header ></Header> -->
  <!-- <Middle  v-bind:ninga="ninga" ></Middle> -->
  <!-- <slot-samp>
    <h1 slot="title">sample data here</h1>
    <p slot="footer">Hello how are you </p>
  </slot-samp>
  <component v-bind:is="sample" v-bind:ninga='ninga'></component>
<button @click="sample='Header'">chnage</button> -->

  <!-- <AddBlog></AddBlog> -->
  <GetAllBlogs></GetAllBlogs>
  <div>

  </div>


</template>

<style scoped></style>
