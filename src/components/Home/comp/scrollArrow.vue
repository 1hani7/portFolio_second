<script setup>

</script>

<style scoped>
.repeater { animation: move 1.5s ease infinite; }
@keyframes move {
    0%{ transform: translateY(-50%); opacity: 1; }
    100%{ transform: translateY(0%); opacity: 0; }
}
</style>

<template>
    <div class="repeater fs-4 position-absolute bottom-0 mb-5">
        <i class="bi bi-chevron-double-down"></i>
    </div>
</template>