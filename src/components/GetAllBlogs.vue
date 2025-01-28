<template>
<ul>
    <li v-for="blog in apiData">
        <h4>{{ blog.title }}</h4>
        <p>{{ blog.id }}</p>
    </li>
</ul>
</template>

<script>
import axios from "axios";


export default {
    data() {
        return {
            apiData: [],
            loding: false,
            error: null,
        }
    },
    created() {
        this.fetchApi();
    },
    methods: {
        async fetchApi(){
            this.loding= true;
            this.error= null
            try{
                const response = await axios.get('https://jsonplaceholder.typicode.com/todos');
                console.log(response);
                this.apiData= response.data.slice(1,10);
            }catch(e){
                this.error=e
            }finally{
                this.error=false;
            }

        }
    }
}

</script>