<script setup>
import {defineProps} from "vue";

defineProps({
    data: Object
})


</script>

<template>
    <section class="car-propose">
        <div class="feature__content container container--pall">
            <h4>{{data.title}}</h4>
            <p>{{data.desc1}}</p>
            <p>{{data.desc2}}</p>
        </div>
    </section>
</template>
