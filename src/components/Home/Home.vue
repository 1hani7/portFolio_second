<script setup>
import Introduce from './comp/introduce.vue'
import DescOne from './comp/descOne.vue'
import DescTwo from './comp/descTwo.vue'
import LinkIcons from './comp/linkIcons.vue'
import ScrollArrow from './comp/scrollArrow.vue'
</script>

<style scoped>
.bgImage {
    background-image: url(../../assets/images/Mask_group.png);
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    opacity: 1;
}

.bgImageOne {
    background-image: url(../../assets/images/gridBg.png);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    filter: grayscale(100%);
    opacity: 0.3;
}
.heightControl { height: 100%; }
.widthControl { width: 35% }

@media (max-width:768px) {
    .bgImage { background-size: 50%; }

    .heightControl { height:40%; }
    .widthControl { width: 100% }
}
</style>

<template>
    <div class="bg-dark">
        <div class="vh-100 container-fluid d-flex flex-column flex-md-row column-gap-md-5
        align-items-center justify-content-center bg-white position-relative overflow-hidden"
            style="border-radius: 0px 0px 100px 100px;">
            <video autoplay loop muted plays-inline
            style="z-index:0; opacity: 0.05; filter: grayscale(100%);
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            min-width: 100%; min-height: 100%;
            width: auto; height: auto;">
                <source src="../../assets/video/codingBg.mp4" />
            </video>
            <div class="order-2 order-md-1 d-flex flex-column align-items-center">
                <Introduce style="z-index:1; mix-blend-mode: difference;" />
                <DescOne style="z-index:1;" />
                <DescTwo style="z-index:1;" />
                <LinkIcons style="z-index:1;" />
            </div>
            <div class="bgImage heightControl widthControl p-0 position-relative order-1 order-md-2"></div>
            <ScrollArrow style="z-index:0;" />
        </div>
    </div>
</template>