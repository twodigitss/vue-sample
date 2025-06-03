<script setup>
    import { ref, watch } from 'vue';
    defineProps({
        user: { type: String, required: true, default: "Defaul User" }
    })
    const count = ref(0);
    const changed = ref(false);
    const goingup = () => {return count.value++}
    const goingdown = () => {return count.value--}
    // const setChanged = () => {return changed.value = !changed.value}

    watch(changed, (newVal) => {
      console.log('Contador cambió:', newVal)
    })

</script>

<template>
    <div class="greetings ">
        <h3>this is the helloworld component</h3>
        <p class="text-green-400"> 
            {{ user }} have successfully created a project with 
        </p>
        <ul>
            <li> <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
            </li>
            <li> <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
            </li>
        </ul>
    </div>
    <div>
        <button @click="goingup">increment</button>
        <button @click="goingdown">decrement</button>
        <button @click="changed = !changed">activate</button>
        <p>{{ count }}</p>
    </div>
</template>

