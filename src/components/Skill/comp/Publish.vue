<script setup>
</script>

<style scoped>
@media (max-width:576px) {
    .smMan { margin: 0 auto; position: relative; top:-35px; }
}
</style>

<template>
    <div class="text-center w-100 bg-body-tertiary border rounded-5 py-5">
        <h3 class="fw-bolder text-secondary mb-4">BASIC</h3>
        <div class="d-flex flex-column flex-sm-row gap-3 justify-content-center">
            <div class="d-flex column-gap-3 mx-auto mx-sm-0">
                <div class="hexagon">
                    <div class="shape">
                        <img src="@/assets/logo/htmlLogo.png" />
                    </div>
                </div>
                <div class="hexagon">
                    <div class="shape">
                        <img src="@/assets/logo/jsLogo.png" />
                    </div>
                </div>
            </div>
            <div class="hexagon d-flex smMan">
                <div class="shape">
                    <img src="@/assets/logo/cssLogo.png" />
                </div>
            </div>
        </div>
    </div>
</template>