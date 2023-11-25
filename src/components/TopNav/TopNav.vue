<script setup>
import NavList from './comp/NavList.vue';
import NavLogo from './comp/NavLogo.vue';

import { onMounted, onUnmounted } from 'vue';

const navBarShowHide = (e) => {
    const navigation = document.querySelector('.navigation');
    if (e.deltaY > 0) { navigation.classList.add('navHide'); }
    else { navigation.classList.remove('navHide'); }
}

onMounted(() => window.addEventListener('wheel', navBarShowHide));
onUnmounted(() => window.removeEventListener('wheel', navBarShowHide));
</script>

<style>
.navHide {
    transform: translateY(-100%)
}
</style>

<template>
    <nav class="navigation container-fluid navbar navbar-expand-lg position-fixed top-0"
    style="transition:0.5s ease;">
        <div class="container-fluid px-3 px-md-5">
            <NavLogo />
            <button class="navbar-toggler" style="border:none; box-shadow:none;" type="button" data-bs-toggle="collapse"
                data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <NavList />
        </div>
    </nav>
</template>