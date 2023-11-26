<script setup>
import ImageSlider from '../comp/ImageSlider.vue';
import { ref, onMounted, onUnmounted } from 'vue';
import axios from 'axios';
const data = ref([]);
const getData = async () => {
    try {
        const response = await axios.get('projects.json');
        data.value = response.data;
    } catch (error) {
        console.error('Error fetching data:', error);
    }
}
onMounted(getData);
</script>

<style scoped>
::-webkit-scrollbar {
    width: 0px;
    height: 0px;
}

.widthControl {
    width: 50%;
}

@media(max-width:992px) {
    .widthControl {
        width: 100%;
    }
}
</style>

<template>
    <div v-for="(v, i) in data" :key="i" class="container-md bg-white mt-5 mb-5 rounded-4 px-3 px-md-5 py-5
    d-flex flex-column align-items-center row-gap-2 shadow">
        <h4 class="fw-bolder display-5" style="white-space: nowrap;">{{ v.title }}</h4>
        <small class="text-secondary">{{ v.date }}</small>
        <div class="row mt-4 w-100">
            <ImageSlider :imgArray="v.image" :index="i" />
            <div class="col-12 col-lg-6 ps-0 ps-lg-4 mt-4 mt-lg-0">
                <p class="">&nbsp;{{ v.desc1 }}</p>
                <p class="">&nbsp;{{ v.desc2 }}</p>
                <div class="d-flex gap-3 my-3 my-lg-0">
                    <a class="btn btn-sm btn-outline-dark align-self-start" :href="v.pHref" target="_blank">
                        사이트 보기 <i class="bi bi-arrow-right-circle"></i>
                    </a>
                    <a class="btn btn-sm btn-outline-dark align-self-start" :href="v.gHref" target="_blank">
                        깃허브 보기 <i class="bi bi-arrow-right-circle"></i>
                    </a>
                </div>
                <div class="d-flex flex-column mt-2">
                    <div class="border-bottom py-1">
                        <div class="fw-bolder mb-1">주요기능</div>
                        <div class="">{{ v.func }}</div>
                    </div>
                    <div class="border-bottom py-1">
                        <div class="fw-bolder mb-1">GitHub</div>
                        <div class="w-100" style="word-break:break-all;">{{ v.gHref }}</div>
                    </div>
                    <div class="border-bottom py-1">
                        <div class="fw-bolder mb-1">URL</div>
                        <div class="w-100" style="word-break:break-all;">{{ v.pHref }}</div>
                    </div>
                    <div class="border-bottom py-1">
                        <div class="fw-bolder mb-1">Skills</div>
                        <div class="w-100">
                            <span class="btn btn-sm btn-dark me-2 mb-1" style="cursor: default"
                                v-for="(value, index) in v.skills">
                                {{ value }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>