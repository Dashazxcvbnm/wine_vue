<template>
<div class="section--third">
    <div class="content-container">
        <div class="border-wrapper">

            <div class="sector-content">

                <WineVueText
                class="section--third-text"
                text="Новинки коллекций"/>

                <div>
                <WineVueTitle
                class="section--third-title"
                text="Март 1980"/>

                <WineVueTitle
                class="section--third-title"
                text="Урожай Марселя"/></div>

                <div class="border-line"></div>

                <WineVueText
                class="section--third-text"
                text="Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Feugiat enim tortor in hac id imperdiet adipiscing.
                Pellentesque nisi, mi sit non sit sed fermentum.
                Felis adipiscing morbi sodales ac."/>

                <SpreadsheetWine
                :items="items"/>

                <WineVueText
                class="section--third-text"
                text="Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Feugiat enim tortor in hac id imperdiet adipiscing.
                Pellentesque nisi, mi sit non sit sed fermentum.
                Felis adipiscing morbi sodales ac."/>

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

import WineVueText from './GUI/WineVueText.vue';
import WineVueTitle from './GUI/WineVueTitle.vue';
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
}

.content-container {
    width: 86%;
    margin: 0 auto;
}

.border-wrapper {
    border-top: 1px solid rgb(153, 132, 49);
    border-bottom:1px solid rgb(153, 132, 49);
    margin: 80px auto 80px auto;
    padding: 64px 0px 60px 0px;
    display: flex;
    justify-content: space-between;
    width: 100%;
    overflow-x: hidden;
}

.sector-content:nth-child(2) {
    margin-left: 125px;
}
.img-wrapper {
    display: flex;
    justify-content: space-between;
    margin-top: 26px;
}

.img-bottom:nth-child(1)  {
    margin-right: 30px;
}

.section--third-text {
    text-align: left;
    margin-bottom: 30px;
    line-height: 21px;
    font-size: 14px;
    width: 445px;
}

.section--third-title {
    color: #282828;
    text-align: left;
}

.section--third-title:nth-child(1) {
    margin-bottom: 0px;
}

.section--third-title:nth-child(2) {
    margin-top: 0px;
}

.border-line {
    border-top: 1px solid #282828;
    width: 160px;
    margin: 28px auto 31px 0px;
}
</style>