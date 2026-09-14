<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])
const newItem = ref('')

// TODO: Add Code Here
function deleteItem(index) {
    // splice --> index position, deleteCount, insertItem
    items.value.splice(index, 1)
}

function addItem() {
    items.value.push(newItem.value)
    // clear the text box after item is pushed
    newItem.value = ''
}


</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item, index) in items" :key="index">
            {{ item }}
            <!-- index is needed when splice() is used -->
            <button @click="deleteItem(index)">Delete!</button>
        </li>
     </ul>
     <br>
     <!-- keydown.enter is when user click enter key, it will be added -->
     <input type="text" v-model="newItem" @keydown.enter="addItem">
     <button @click="addItem">Add!</button>
</template>
