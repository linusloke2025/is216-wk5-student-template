<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const newItem = ref('')
function add() {
    items.value.push(newItem.value)
    newItem.value = ''
}

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item, index) in items" :key="index">
        {{ item }}
    <button @click="items.splice(index, 1)">Delete</button>
    </li>
</ul>
<input type="text" v-model="newItem"><button @click="add()">Add</button>
   
</template>
