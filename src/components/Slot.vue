<template>
   <div>
<h1>Sample test data {{hello }}</h1>
<slot></slot>
   </div>
</template>

<script>
export default {
    data(){
        return {
            hello :"sample"
        }
    }
}
</script>


<style scoped></style>
