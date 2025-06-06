<script setup>
    import { RouterLink, RouterView } from 'vue-router'
    import HelloWorld from './components/HelloWorld.vue'
    import Form from './components/Form.vue'
</script>

<template>
    <header>
        <div class="wrapper">
            <nav class="flex bg-gray-100 gap-1 p-2">
                <RouterLink to="/">Home</RouterLink> <br/>
                <RouterLink to="/about">About</RouterLink>
            </nav>

            <RouterView />

            <Form/>

        </div>
    </header>

</template>

<style global>
    /* @import "tailwindcss"; */
    :root{
        font-family: "Inter", Arial, "Noto Sans", sans-serif;
    }
</style>
