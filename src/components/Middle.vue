<template>
    <ul>
        <li v-for="ningas in ninga" @click="ningas.show = !ningas.show">
            <h1>{{ ningas.name }}</h1>
            <p v-show="ningas.show">{{ ningas.discription }}</p>
        </li>
    </ul>
</template>


<script>
export default {
    props: {
        ninga:
        {
            type: Array
        }
    },
    data() {
        return {
            // ninga:
            //     [
            //         { name: "harsh", discription: "the is good ", show: false },
            //         { name: "muskan", discription: "she is good ", show: false },
            //         { name: "daksh", discription: "he is good ", show: false },
            //     ]
        }
    }
}

</script>