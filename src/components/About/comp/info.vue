<script setup>
const list = [
    {title: 'Name', icon: 'person', val: '신상수'},
    {title: 'Email', icon: 'envelope-paper', val: '1hani7@gmail.com'},
    {title: 'Age', icon: 'calendar-check', val: '만 26세 / 1997년'},
    {title: 'Tel', icon: 'telephone', val: '010-4378-8589'},
]
</script>

<template>
    <div class="ms-1 row row-cols-2 w-100 text-white row-gap-3">
        <div v-for="(v, i) in list" :key="i"
        class="col border-end p-0"
        :class="{ 'ps-3': i % 2 !== 0 }">
            <div class="d-flex column-gap-1 mb-1">
                <i :class="`bi bi-${v.icon}`"
                style="width:20px"></i>
                <div class="">{{ v.title }}</div>
            </div>
            <div class="text-white-50 ps-0">{{ v.val }}</div>
        </div>
    </div>
</template>