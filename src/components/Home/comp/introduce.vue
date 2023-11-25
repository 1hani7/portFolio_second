<script setup>
</script>

<style>
.lineAni {
    stroke-dasharray: 400;
    stroke-dashoffset: 400;
    animation: drawPath 6s ease infinite;
}

@keyframes drawPath {
    to {
        stroke-dashoffset: 0;
    }
}
</style>

<template>
    <div class="text-center d-flex flex-column row-gap-3 row-gap-sm-0 text-white">
        <small class="fs-6">안녕하세요!</small>
        <h2 class="d-flex flex-column flex-sm-row align-items-end m-0">
            <div class="me-xs-0 me-sm-3 mb-2 mb-sm-0"
            style="white-space: nowrap;">
                프론트엔드 개발자
            </div>
            <div class="position-relative d-flex align-items-end mb-2 mb-sm-0">
                <svg class="position-absolute"
                width="180" height="69" viewBox="0 0 142 69"
                style="left:-40px; top:-10px;"
                    xmlns="http://www.w3.org/2000/svg">
                    <path class="lineAni" d="M0.428793 65.7085C6.92469 
                        64.0885 119.212 70.0351 137.452 30.755C152.732 -2.14979 
                        98.0584 -1.07598 72.7721 7.56929C49.5778 15.4994 -43.2736 
                        54.8449 109.198 66.9284" stroke="#0d6efd80"
                        stroke-width="3" fill="transparent" />
                </svg>
                <strong class="fs-1" style="white-space: nowrap;">신상수</strong>
                <div class="ms-3" style="white-space: nowrap;">입니다.</div>
            </div>
        </h2>
    </div>
</template>