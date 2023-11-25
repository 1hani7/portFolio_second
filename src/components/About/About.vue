<script setup>
import Photo from './comp/photo.vue';
import Info from './comp/info.vue';
import Desc from './comp/desc.vue';
</script>

<style>
@media(max-width:992px) {
    .heightControl { height:100%; }
    .widthControl { width:75%; }}
@media(min-width:992px) {
    .heightControl { height:100vh; }
    .widthControl { width:955px; max-width: 955px; }
}
</style>

<template>
    <div class="heightControl w-w-100 bg-dark py-5
    d-flex align-items-center justify-content-center"
    style="border-radius: 0px 100px 0px 100px;">
        <div class="widthControl d-flex flex-column flex-lg-row align-items-center">
            <Photo class="mb-5 mb-lg-0 me-0 me-lg-5 align-self-center align-self-lg-start" />
            <div class="ms-0 ms-lg-5">
                <Desc />
                <hr class="text-white" />
                <Info />
            </div>
        </div>
    </div>
</template>