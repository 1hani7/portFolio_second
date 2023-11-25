<script setup>

</script>

<style scoped>
.shadow-set {
    box-shadow:10px 10px 0px #0d6efd, -10px -10px 0px #70c5fd;
    transition: 0.5s ease;
}
.shadow-set:hover {
    box-shadow:40px 40px 0px #0d6efd80, -40px -40px 0px #70c5fd80;
}
.setGray{ filter:grayscale(100%); }
.setGray:hover{ filter:grayscale(0%); }
</style>

<template>
    <div class=" flex-shrink-0 shadow-set overflow-hidden
    d-flex align-items-end justify-content-center"
    style="width:300px; height:450px;">
        <img
        class="setGray"
        style="height:90%; transition: 0.5s ease;"
        src="@/assets/images/profile.png" />
    </div>
</template>