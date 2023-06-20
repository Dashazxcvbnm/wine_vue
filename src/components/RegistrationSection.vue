<template>
<div class="section--fourth">
    <div class="content-container">

        <div class="title-wrapper">

            <h1 
            class="section--fourth-title">
            Запись на дегустацию</h1>

            <img 
            class="section-fourth__img" 
            src="../../image/SectionFourthImgLeft.png">

            <img 
            class="section-fourth__img" 
            src="../../image/SectionFourthImgRight.png">

        </div>
    
        <div class="border-wrapper">

            <div class="inner_content-container">
                <div class="border-line"></div>

                <span 
                class="section-text_white">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
                Feugiat enim tortor in hac id imperdiet adipiscing. 
                Pellentesque nisi, mi sit non sit sed fermentum.</span>

                <RegistrationForm
                class="form-wrapper"/>

            </div>

        </div>
    </div>
</div>
</template>

<script setup>
import RegistrationForm from './RegistrationForm.vue';

</script>

<style scoped>

.section--fourth {
    background: #282828;
    min-height: 767px;
    align-items: center;
    display: flex;
    padding-top: 17px;
}

.content-container {
    width: 86%;
    margin: 0 auto;
}

.border-wrapper {
    border: 3px solid #c4c4c4;
    display: flex;
    justify-content: space-around;
    width: 1110px;
    min-height: 538px;
    height: 1px;
}

.inner_content-container {
    width: 49%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 65px 0;
    height: 70%;
}

.title-wrapper {
    position: relative;
}

.section--fourth-title {
    position: absolute;
    top: -48px;
    left: 300px;
    width: 490px;
    background-color: #282828;
    text-align: center;
}

.section-fourth__img {
    position: absolute;
}

.section-fourth__img:nth-child(2) {
    left: -25px;
    top: -70px;
}

.section-fourth__img:nth-child(3) {
    left: 910px;
    top: -65px;
}

.border-line {
    border: 1px solid #FFFFFF;
    width: 118px;
    margin: 0 auto;
}

.form-wrapper {
    height: 53%;
}

.section-text_white {
    padding-bottom: 30px;
    text-align: center;
}
</style>