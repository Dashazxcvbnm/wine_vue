<template>
    <div class="header">
        <span>{{ add }}</span>
        <span>{{ phone }}</span>
    </div>
</template>

<script setup>

defineProps({
    add: [String, Number],
    phone: [String, Number]
})

</script>

<style scoped>

.header {
    display: flex;
    justify-content: space-between;
    font-size: 13px;
    padding-top: 30px;
    padding-bottom: 20px;
    font-family: 'Montserrat';
    line-height: 19.5px
}
</style>