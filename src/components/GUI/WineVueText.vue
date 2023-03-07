<template>
    <div>
        <div class="section-text">{{ text }}</div>
    </div>
</template>

<script setup>

defineProps({
    text: String
})

</script>

<style scoped>

.section-text {
    font-family: 'Montserrat';
    /* line-height: 24px;
    text-align: center; */
}
</style>