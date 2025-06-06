<script setup>
import { ref } from 'vue'

const name = ref("")
const fileInput = ref(null)
const selectedFile = ref(null)

const onFileChange = () => {
  const file = fileInput.value?.files[0]
  selectedFile.value = file
  console.log('Selected file:', file)
}
</script>

<template>
  <form>
    <div class="form-group">
      <label>Name:</label>
      <input type="text" v-model="name" class="form-control" />
    </div>
    
    <div class="form-group">
      <label>Email:</label>
      <input type="email" v-model="email" class="form-control" />
    </div>

    <input type="file" ref="fileInput" @change="onFileChange" /> <br/>

    <button type="submit">Submit</button>
  </form>

  <p v-if="name">Hello, {{ name }}!</p>
  <p v-if="selectedFile">File selected: {{ selectedFile.name }}</p>
</template>

