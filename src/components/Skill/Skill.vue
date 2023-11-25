<script setup>
import SkillTitle from './comp/SkillTitle.vue';
import Publish from './comp/Publish.vue';
import Framework from './comp/Framework.vue';
import StateMan from './comp/StateMan.vue'
import StyleFramework from './comp/StyleFramework.vue';
import DataWork from './comp/DataWork.vue';
import Library from './comp/Library.vue';
import ETC from './comp/ETC.vue';
</script>

<style>
.hexagon {
    position: relative;
    width: 170px;
    max-width: 170px;
    max-height: 200px;
    transition: 0.75s ease;
    filter: drop-shadow(0px 10px 10px #ababab);
}

.hexagon::after {
    content: "";
    display: block;
    padding-bottom: 100%;
}

.hexagon:hover {
    transform: translateY(-9%);
}

.hexagon .shape {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    clip-path: polygon(0 25%, 50% 0, 100% 25%, 100% 75%, 50% 100%, 0 75%);
    background: white;
    display: flex;
    align-items: center;
    justify-content: center;
}

.hexagon .shape img {
    position: relative;
    top: 10px;
    width: 65%;
}

.geoBg {
    background-image: url(../../assets/images/skillBg.png);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    z-index: 0;
    background-attachment: fixed;
}
</style>

<template>
    <div class="pt-5 container-md d-flex flex-column
    align-items-center justify-content-center bg-white
    row-gap-5 position-relative"
    style="padding-bottom:300px;">
        <SkillTitle />
        <Publish />
        <Framework />
        <StateMan />
        <Library />
        <StyleFramework />
        <DataWork />
        <ETC />
        <div class="geoBg position-absolute"></div>
    </div>
</template>