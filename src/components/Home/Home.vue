<script setup>
import Introduce from './comp/introduce.vue'
import DescOne from './comp/descOne.vue'
import DescTwo from './comp/descTwo.vue'
import LinkIcons from './comp/linkIcons.vue'
import ScrollArrow from './comp/scrollArrow.vue'
</script>

<style></style>

<template>
    <div class="bg-dark">
        <div class="vh-100 container-fluid d-flex flex-column
        align-items-center justify-content-center bg-white"
        style="border-radius: 0px 0px 0px 100px;">
            <Introduce />
            <DescOne />
            <DescTwo />
            <LinkIcons />
            <ScrollArrow />
        </div>
    </div>
</template>