<script setup>
import {defineProps} from "vue";

defineProps({
    menu: Array
})
</script>

<template>
    <footer class="footer">
        <div class="footer-flex">
            <div class="header__links">
                <a v-for="item in menu" href="#">{{item}}</a>
                <p class="footer-copy">©2021 Cash for Cars | Terms and Conditions | Privacy Policy</p>
            </div>
            <div class="footer__logo">
                <a href="/">
                    <img src="../assets/images/logo.svg" alt="Easybank"/>
                </a>
            </div>
        </div>
    </footer>
</template>
