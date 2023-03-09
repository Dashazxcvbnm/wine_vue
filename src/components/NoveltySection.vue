<template>
<div class="section--third">
    <div class="content-container">
        <div class="border-wrapper">

            <div class="sector-content">

                <span 
                class="section--third-text section-text_black">
                Новинки коллекций</span>

                <h1 
                class="section--third-title">
                    Март 1980<br/>
                    Урожай Марселя<br/>
                </h1>

                <div class="border-line"></div>

                <span
                class="section--third-text section-text_black"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Feugiat enim tortor in hac id imperdiet adipiscing.
                Pellentesque nisi, mi sit non sit sed fermentum.
                Felis adipiscing morbi sodales ac.</span>

                <SpreadsheetWine
                :items="items"/>

                <span
                class="section--third-text section-text_black"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Feugiat enim tortor in hac id imperdiet adipiscing.
                Pellentesque nisi, mi sit non sit sed fermentum.
                Felis adipiscing morbi sodales ac.</span>

                <WineVueButton 
                text="узнать подробнее"/>
            </div>

            <div class="sector-content">

                <img src="..//../Image/SectionThirdImgTop.jpg">

            <div class="img-wrapper">
                <img class="img-bottom" src="..//../Image/SectionThirdImgUnderLeft.jpg">
                <img src="..//../Image/SectionThirdImgUnderRight.jpg">
            </div>

            </div>

        </div>
    </div>
</div>
</template>

<script setup>

import WineVueButton from './GUI/WineVueButton.vue';
import SpreadsheetWine from './GUI/SpreadsheetWine .vue'

import { ref } from 'vue'

const items = ref([
  { age: 1980, 
    subtitle: 'Colli Euganei Bianco Ca Lustra 1980', 
    text: 'Красочная бутылка вина из Марселя' },
  { age: 1980, 
    subtitle: 'Colli Euganei Bianco Ca Lustra 1980', 
    text: 'Красочная бутылка вина из Марселя' },
  { age: 1980, 
    subtitle: 'Colli Euganei Bianco Ca Lustra 1980', 
    text: 'Красочная бутылка вина из Марселя' },
])
</script>

<style scoped>

.section--third {
    background: rgb(230, 227, 196);
    display: flex;
    align-items: center;
    min-height: 1038px;
}

.content-container {
    width: 86%;
    margin: 0 auto;
}

.border-wrapper {
    border-top: 1px solid rgb(153, 132, 49);
    border-bottom: 1px solid rgb(153, 132, 49);
    display: flex;
    justify-content: space-between;
    width: 100%;
    overflow-x: hidden;
}

.sector-content {
    padding: 60px 0 60px 0;
}

.sector-content:nth-child(1) {
   flex-basis: 40%;
   display: flex;
   flex-direction: column;
   justify-content: space-between;
}

.section--third-text:nth-child(1) {
    font-size: 16px;
}

.img-wrapper {
    display: flex;
    justify-content: space-between;
    margin-top: 26px;
}

.img-bottom:nth-child(1)  {
    margin-right: 30px;
}

.section--third-title {
    color: #282828;
    text-align: left;
    margin: 0;
}

.border-line {
    border-top: 1px solid #282828;
    width: 160px;
}
</style>