<template>
 <div>
    <ContentWrapper class="section--first">

        <PageHeader add="Новокузнечный переулок 4/1" phone="8 (812) 123-45-67"></PageHeader>

        <MenuItem :items="items"></MenuItem>

        <div class="button-wrapper">
            <ButtonShape class="control-button">винная карта</ButtonShape>
            <ButtonShape class="control-button">дегустация</ButtonShape>
        </div>

    </ContentWrapper>
 </div>
</template>

<script setup>

import ContentWrapper from '../components/ContentWrapper.vue';
import PageHeader from '../components/GUI/PageHeader.vue';
import MenuItem from '../components/GUI/MenuItem.vue';
import ButtonShape from '../components/GUI/ButtonShape.vue';

import { ref } from 'vue'

const items = ref([
  { id: 1, value: 'Каталог' },
  { id: 2, value: 'Доставка' },
  { id: 3, value: 'Коллекции' },
  { id: 4, value: 'Контакты' },
])

</script>

<style scoped>

.section--first {
    background-image: url(../Image/SectionFirstFon.jpg);
    background-size: cover;
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


