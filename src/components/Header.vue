<script>
    import Button from './Button.vue'
    import "./Header.css"
    export default {
        props: ['create', 'add', 'deleteTab', 'createImg', 'deleteImg'],
        components: {
            Button,
        }
    }
</script>

<template>
    <div class="header">
        <Button title="Stwórz 1000 wierszy" @click="create(1000)"/>
        <Button title="Stwórz 10 000 wierszy" @click="create(10000)"/>
        <Button title="Dodaj 1000 wierszy" @click="add(1000)"/>
        <Button title="Dodaj 10 000 wierszy" @click="add(10000)"/>
        <Button title="Usuń tabelę" @click="deleteTab()"/>
        <Button title="Wstaw 300 zdjęć" @click="createImg(300)"/>
        <Button title="Wstaw 700 zdjęć" @click="createImg(700)"/>
        <Button title="Usuń zdjęcia" @click="deleteImg()"/>
    </div>
</template>

