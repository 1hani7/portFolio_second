/**eslint-disable */
<script>
import { ref, onMounted } from 'vue';
export default {
    props: {
        imgArray: Array,
        index: Number
    },
    setup(props){
        const dt = props.imgArray;
        const idx = props.index;


        // 무한루프 슬라이더
        const autoS = () => {
            const slider = document.querySelectorAll('.slider')[idx];
            if( slider.scrollWidth /2 <= slider.scrollLeft ) slider.scrollLeft = 0;
            slider.scrollLeft += 1;
            setTimeout(() => {
                autoS();
            },10);
        }

        onMounted(autoS);

        return { dt }
    }
}
</script>

<template>
    <div class="slider widthControl d-flex col-12 col-lg-6 bg-dark rounded-5 overflow-scroll p-0
            align-items-center position-relative" style="height:450px;">
        <div class="d-flex h-100 align-items-center position-absolute top-0 left-0">
            <img v-for="(val, ix) in dt" :key="val" :src="val" alt="img" class="me-2" style="height:100%" />
            <img v-for="(val, ix) in dt" :key="val" :src="val" alt="img" class="me-2" style="height:100%" />
        </div>
    </div>
</template>