<template>
    <h1 class="rext-w">{{ title }}</h1>
    <p class="read-the-docs">Click on the Vite and Vue logos to learn more {{ sample1 }}</p>
</template>


<script>
export default {
data(){
    return{
        title :"sample",
        sample1:"Harsh"
    }
}
}
</script>


<style scoped>
.rext-w {
    color: azure;
}
</style>