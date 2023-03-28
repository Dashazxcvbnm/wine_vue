<template>
    <div>
        <button class="btn">{{ text }}</button>
    </div>
</template>

<script setup>

defineProps({
    text: String
})

</script>

<style scoped>

.btn {
    background: #998431;
    color: #ffffff;
    padding: 15px 30px;
    border: none;
    font-size: 16px;
    line-height: 20px;
    font-family: 'Montserrat';
    text-transform: uppercase;
    cursor: pointer;
    white-space: nowrap;
}
</style>