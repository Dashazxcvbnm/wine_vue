<template>
    <h1 class="section-title">{{ text }}</h1>
</template>

<script setup>

defineProps({
    text: String
})

</script>

<style scoped>

.section-title {
    font-family: 'Playfair Display';
    font-size: 30px;
    color: rgb(255, 255, 255);
    text-align: center;
    line-height: 54px;
}
</style>