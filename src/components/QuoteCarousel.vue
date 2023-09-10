<script setup>
import {defineProps} from "vue";

defineProps({
    quotes: Object
})

</script>

<template>
    <div class="item-feedback">
        <div>"Can't recommend them enough. Their fast, friendly service was ideal, and they offered
            us a better price than other trade in sites..."</div>
        <form class="form-radio-inline" action="#">
            <label>
                <input name="group1" type="radio"/>
            </label>
            <label>
                <input name="group1" type="radio" checked />
            </label>
            <label>
                <input class="with-gap" name="group1" type="radio"  />
            </label>
            <label>
                <input name="group1" type="radio" disabled="disabled" />
            </label>
        </form>
    </div>
</template>
