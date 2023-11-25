<script setup>

</script>

<style scoped>
@media (max-width:576px) {
    .smMan2 { margin: 0 auto; position: relative; top:-65px; }
    .smMan { margin: 0 auto; position: relative; top:-40px; }
}
@media (min-width:576px) {
    .smMan2 { margin: 0 auto; position: relative; top:-20px; }
    .smMan { margin: 0 auto; position: relative; top:0px; }
}
</style>

<template>
    <div class="text-center w-100 bg-body-tertiary border rounded-5 py-5">
        <h3 class="fw-bolder text-secondary mb-4">AND...</h3>
        <div class="d-flex flex-column justify-content-center">
            <div class="d-flex flex-column flex-sm-row gap-3 mx-auto">
                <div class="d-flex column-gap-3">
                    <div class="hexagon">
                        <div class="shape">
                            <img src="@/assets/logo/canvaLogo.png" style="top:0px;" />
                        </div>
                    </div>
                    <div class="hexagon">
                        <div class="shape">
                            <img src="@/assets/logo/figma.png" style="top:0;" />
                        </div>
                    </div>
                </div>
                <div class="hexagon d-flex smMan">
                    <div class="shape">
                        <img src="@/assets/logo/ts.png" style="top:0;" />
                    </div>
                </div>
            </div>
            <div class="d-flex gap-3 justify-content-center
            position-relative smMan2">
                <div class="hexagon">
                    <div class="shape">
                        <img src="@/assets/logo/aiLogo.png" style="top:0;" />
                    </div>
                </div>
                <div class="hexagon">
                    <div class="shape">
                        <img src="@/assets/logo/photoshopLogo.png" style="top:0;" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>