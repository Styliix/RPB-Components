<script setup>
import QuickPill from './QuickPill.vue';


import { ref } from 'vue'

const parentMessage = ref('Parent')
const items = ref([{ message: 'Foo' }, { message: 'Bar' }, { message: 'Bar' }])
</script>

<template>  
    <h1>TEST</h1>
    <h2>TEST</h2>
    <a>Alle Länder</a>
    <div class="test">
        <QuickPill 
            v-for="pill in items"
        />
    </div>
</template>

<style scoped>
h1 {
    margin-left: 20px;
    margin-top: 50px;
}
h2 {
    margin-left: 22px;
    margin-top: -10px;
    margin-bottom: 50px;
}
a {
    margin-top: -60px;
    float: right;
    font-size: 14px;
    margin-right: 30px;
    margin-top: -100px;
}

.test {
    width: 100%;
    height: 30vh;
    padding-left: auto;
    padding-right: auto;
}

@media (min-width: 1901px) {
    .test {
    width: 100%;
    height: 30vh;
    padding-left: auto;
    padding-right: auto;
    display: flex;
}
}
</style>

