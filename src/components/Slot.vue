<template>
   <div>
<slot name='title'></slot>
<h1>Sample test data {{hello }}</h1>
<slot name='footer'>{hello } {{hello}}</slot>
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
