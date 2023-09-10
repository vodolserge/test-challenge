<script setup>
import {defineProps} from "vue";

defineProps({
    chevronData: Object
})


</script>

<template>
    <div class="feature">
        <img :src="chevronData.image" :alt="chevronData.title"/>
        <h3>{{chevronData.title}}</h3>
        <p>{{chevronData.description}}</p>
    </div>
</template>
