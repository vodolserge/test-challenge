<script setup>
import {defineProps} from "vue";

defineProps({
    options: Array
})
</script>

<template>
    <section class="car-options">
        <div class="options-flex">
            <div class="options-item" v-for="item in options">
                <ul>
                    <li v-for="option in item">{{option}}</li>
                </ul>
            </div>
        </div>
    </section>
</template>
