<template>

    <input 
    class="input-form"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    />

</template>

<script setup>

const props = defineProps(['modelValue']);
const emits = defineEmits(['update:modelValue']);

</script>

<style scoped>

.input-form {
    font-size: 13px;
    font-family: 'Montserrat';
    background-color: rgb(40, 40, 40);
    color: rgb(255, 255, 255);
    border: none;
    border-bottom: 1px solid rgb(255, 255, 255);
    outline: none;
    padding-bottom: 10px;
}
</style>