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
    background-color: #282828;
    color: #ffffff;
    border: none;
    border-bottom: 1px solid #ffffff;
    outline: none;
    padding-bottom: 10px;
}
</style>