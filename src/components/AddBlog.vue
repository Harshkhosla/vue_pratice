<template>
    <div>
        <h1> {{ title }} </h1>
        <input type="text" required v-model="title" />
        <p>{{ discription }}</p>
        <textarea v-model="discription"></textarea>
        <div>
            <label for="">Sample</label>
            <input type="checkbox" v-model="containers" value="Harsh" />
            <label for="">Sample</label>
            <input type="checkbox" v-model="containers" value="Muskan" />
        </div>
        <div>
            <ul>
                <li v-for='container in containers'>{{ containers }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: "sample blogs",
            discription: "this is blog discription",
            containers: [],
        }
    }
    ,
    methods: {
        post() {
            this.$http.post('http://localhost:5000/harsh', {
                tutle: this.title,
                discription: this.discription
            }).then(res(data)(
                console.log(data)
            )).catch(error)(
                console.log(error)
            )
        }
    }
}

</script>