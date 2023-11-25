<script setup>
const list = [
    { name: 'HOME' },
    { name: 'ABOUT' },
    { name: 'SKILL' },
    { name: 'PROJECTS' },
    { name: 'EXPERIENCE' },
    { name: 'TOYS' },
]

const showUnderLine = (e) => e.target.nextSibling.classList.toggle('d-none');
const hideUnderLine = (e) => e.target.nextSibling.classList.toggle('d-none');

</script>
<style scoped>
.widthControl {
    animation: widthControl 0.5s ease forwards;
}

@keyframes widthControl {
    0% {
        width: 0%;
    }

    100% {
        width: 100%;
    }
}
</style>

<template>
    <div class="collapse navbar-collapse pt-3 pt-md-0" id="navbarSupportedContent">
        <ul class="navbar-nav mb-2 mb-lg-0 ms-auto d-flex column-gap-4">
            <li v-for="(item, idx) in list" :keys="idx" class="nav-item act position-relative">
                <a @mouseover="showUnderLine" @mouseleave="hideUnderLine" class="nav-link" :href="`#${item.name}`"
                style="mix-blend-mode: difference;">
                    {{ item.name }}
                </a>
                <div class="widthControl border-bottom d-none m-0 p-0"></div>
            </li>
        </ul>
    </div>
</template>