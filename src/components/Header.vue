<script setup>
import {onMounted, defineProps} from "vue";

defineProps({
    menu: Array
})

onMounted(() => {
    const btnHamburger = document.querySelector('#btnHamburger');
    const body = document.querySelector('body');
    const header = document.querySelector('.header');
    const fadeElems = document.querySelectorAll('.has-fade');

    btnHamburger.addEventListener('click', function () {
        console.log('click hamburger');

        if (header.classList.contains('open')) {
            body.classList.remove('noscroll');
            header.classList.remove('open');
            fadeElems.forEach(function (element) {
                element.classList.remove('fade-in');
                element.classList.add('fade-out');
            });

        } else {
            body.classList.add('noscroll');
            header.classList.add('open');
            fadeElems.forEach(function (element) {
                element.classList.remove('fade-out');
                element.classList.add('fade-in');
            });

        }
    });
})

</script>

<template>
    <header class="header">
        <nav class="container container--pall flex flex-jc-sb flex-ai-c">
            <a href="/" class="header__logo">
                <img src="../assets/images/logo.svg" alt="Easybank" />
            </a>

            <a id="btnHamburger" href="#" class="header__toggle hide-for-desktop">
                <span></span>
                <span></span>
                <span></span>
            </a>

            <div class="header__links hide-for-mobile">
                <a v-for="item in menu" href="#">{{item}}</a>
            </div>
        </nav>

        <div class="header__menu has-fade">
            <a v-for="item in menu" href="">{{item}}</a>
        </div>
    </header>
</template>
