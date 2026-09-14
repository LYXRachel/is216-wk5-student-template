<script setup>

import { ref } from 'vue';

const id = ref('circle')
// const cls = ref('circle')


function mOver() {
    // add code here
    id.value = "square"
}

function mOut() {
    // add code here
    id.value = "circle"
   
}
</script>

<template>
    <!-- modify code below -->
    <!--<div id="shape" class="shape" :class="cls" @mouseover="mOver" @mouseout="mOut">-->
    <div :id="id" @mouseover="mOver" @mouseout="mOut">
        Mouse Over Me
    </div>

</template>

<style scoped>

/*
.shape {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

.circle {
    border-radius: 50%;
}

.square {
    border-radius: 0%;
}
*/

#square {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

#circle {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

</style>