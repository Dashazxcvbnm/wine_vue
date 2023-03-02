<template>
    <div class="border-wrapper">
        <h1 class="section-title">{{ title }}</h1>
        <span>{{ text }}</span>
       <slot> <span></span></slot>
    </div>
</template>

<script setup>

defineProps(['title', 'line', 'text'])

</script>

<style>

.border-wrapper {
    border: 3px solid rgb(196, 196, 196);
    min-height: 600px;
    margin-top: 100px;
    margin-bottom: 100px;
}

.section-title {
    font-family: 'Playfair Display';
    font-size: 30px;
    color: rgb(255, 255, 255);
}
</style>