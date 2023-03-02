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

    <ContentWrapper class="section--second">
        <BorderContentConteiner
        title="Лучший вкус, это вкус долголетнего вина"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
        Feugiat enim tortor in hac id imperdiet adipiscing. 
        Pellentesque nisi, mi sit non sit sed fermentum. 
        Felis adipiscing morbi sodales ac. 
        Mauris dictumst risus pulvinar blandit elit. 
        Vestibulum quam ultrices nascetur et viverra suscipit. 
        Proin vitae aliquet leo aliquam amet rutrum. 
        Lectus auctor purus ultrices enim ultrices. 
        Augue fringilla tellus tortor orci ultrices sed. 
        Viverra cras sapien, pellentesque viverra malesuada. 
        Tellus dolor, eget vitae dignissim molestie eget sit duis. 
        Vitae dui vel pretium euismod diam. 
        Pellentesque amet, lacus, amet, quis risus. 
        Pellentesque scelerisque nunc, orci aliquam quis."
        class="section--second-title">
        <span>'isdnvecioun'</span>
        </BorderContentConteiner>
    </ContentWrapper>

 </div>
</template>

<script setup>

import ContentWrapper from '../components/ContentWrapper.vue';
import PageHeader from '../components/GUI/PageHeader.vue';
import MenuItem from '../components/GUI/MenuItem.vue';
import ButtonShape from '../components/GUI/ButtonShape.vue';
import BorderContentConteiner from '../components/BorderContentConteiner.vue';

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

.section--second {
    background: rgb(40, 40, 40);
    min-height: 856px;
    display: flex;
}

.section--second-title {
}

</style>


