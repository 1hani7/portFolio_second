<script setup>
import Photo from './comp/photo.vue';
import Info from './comp/info.vue';
import Desc from './comp/desc.vue';
</script>

<style>
.bg {
    background-image: url(../../assets/images/introBg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    filter: grayscale(100%);
    z-index: 0;
    background-attachment: fixed;
}
@media(max-width:992px) {
    .heightControl { height:100%; padding: 200px 0; }
    .widthControl { width:75%; }}
@media(min-width:992px) {
    .heightControl { height:100vh; }
    .widthControl { width:955px; max-width: 955px; }
}
</style>

<template>
    <div class="heightControl w-100 bg-dark position-relative
    d-flex align-items-center justify-content-center">
        <div class="heightControl bg w-100 h-100 position-absolute p-0 top-0"></div>
        <div class="widthControl d-flex flex-column flex-lg-row
        align-items-center h-100"
        style="z-index:1;">
            <div class="">
                <Photo class="mb-5 mb-lg-0 me-0 me-lg-5 align-self-center align-self-lg-start" />
            </div>
            <div class="ms-0 ms-lg-5 bg-dark p-3 p-sm-4 w-100 h-100
            rounded rounded-sm-0
            d-flex flex-column justify-content-center">
                <Desc />
                <hr class="text-white" />
                <Info />
            </div>
        </div>
    </div>
</template>