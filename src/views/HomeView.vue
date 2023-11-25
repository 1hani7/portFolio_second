<script setup>
import Home from '../components/Home/Home.vue';
import About from '../components/About/About.vue';
import Skill from '../components/Skill/Skill.vue';

import { ref, onMounted, onUnmounted } from 'vue';




// 현재 페이지 부각
const nowPageIdx = () => {
    const s = window.scrollY;
    const nms = document.querySelectorAll('.nms');
    const Home = document.querySelector('#Home').offsetTop;
    const About = document.querySelector('#About').offsetTop;
    const Skill = document.querySelector('#Skill').offsetTop;
    const configAmount = 400;

    if (s >= Home - configAmount && s < About - configAmount) {
        initSize();
        nms[0].classList.add('fw-bolder');
        nms[0].classList.add('fs-1');
    } else if (s >= About - configAmount && s < Skill - configAmount) {
        initSize();
        nms[1].classList.add('fw-bolder');
        nms[1].classList.add('fs-1');
    } else if (s >= Skill - configAmount) {
        initSize();
        nms[2].classList.add('fw-bolder');
        nms[2].classList.add('fs-1');
    }
}

// 다른 페이지 부각 효과 없앰
const initSize = () => {
    const nms = document.querySelectorAll('.nms');
    nms.forEach((v, i) => {
        v.classList.remove('fw-bolder');
        v.classList.remove('fs-1');
    })
}

onMounted(() => {
    window.addEventListener('scroll', nowPageIdx);

    // 초기값
    const nms = document.querySelectorAll('.nms');
    nms[0].classList.add('fw-bolder');
    nms[0].classList.add('fs-1');
})
onUnmounted(() => {
    window.removeEventListener('scroll', nowPageIdx);
})

</script>

<template>
    <div class="">
        <Home id="Home" />
        <About id="About" />
        <Skill id="Skill" />

        <div class="position-fixed text-white text-end" style="z-index: 10; top:50%; right:20px;
        mix-blend-mode: difference;">
            <div class="nms" style="transition:1s ease;">01.</div>
            <div class="nms" style="transition:1s ease;">02.</div>
            <div class="nms" style="transition:1s ease;">03.</div>
        </div>
    </div>
</template>
