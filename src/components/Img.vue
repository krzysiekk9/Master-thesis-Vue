<script >
    export default {
        props: ["element"],
        methods: {
            getImgUrl(pic) {
                let images = require.context('../assets/pokemon_jpg', false, /\.jpg$/)
                return images('./' + pic + ".jpg")
            }
        }
    }
</script>

<template>
    <img :src="getImgUrl(element)" v-bind:alt="element  " />
</template>


