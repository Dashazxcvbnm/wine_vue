<template>
<div class="section--first">
    <div class="content-container">

        <slot></slot>
        
        <div class="button-wrapper">
            <WineVueButton class="control-button" text="винная карта"></WineVueButton>
            <WineVueButton class="control-button" text="дегустация"></WineVueButton>
        </div>
        
    </div>
</div>
</template>

<script setup>

import WineVueButton from './GUI/WineVueButton.vue';

</script>

<style scoped>

.content-container {
    width: 87%;
    margin: 0 auto;
    height: 100vh;
}

.section--first {
    background-image: url(../Image/SectionFirstFon.jpg);
    background-repeat: no-repeat;
    color: rgb(255, 255, 255);
    min-height: 900px;
}

.button-wrapper {
    display: flex;
    justify-content: center;
    margin-top: 568px;
}

.control-button {
    margin: 15px;
}
</style>