<template>
<div class="section--second">
    <div class="content-container">
        <div class="border-wrapper">

            <WineVueTitle 
            class="section--second-title" 
            text="Лучший вкус, это вкус долголетнего вина"/>

            <div class="border-line"></div>

            <WineVueText
            class="section--second-text"
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
                 Pellentesque scelerisque nunc, orci aliquam quis."/>
                 
            <div class="section-img">
                    
            <img src="..//../Image/SectionSecondImage.png">

            </div>
        </div>
    </div>
</div>
</template>

<script setup>
import WineVueTitle from './GUI/WineVueTitle.vue';
import WineVueText from './GUI/WineVueText.vue';
</script>

<style scoped>

.section--second {
    background: rgb(40, 40, 40);
    display: flex;
    min-height: 856px;
}

.content-container {
    width: 87%;
    margin: 0 auto;
    
}

.border-wrapper {
    border: 3px solid rgb(196, 196, 196);
    margin-top: 100px;
    margin-bottom: 100px;
}

.section--second-title {
    margin: 60px auto 40px auto;
}

.border-line {
    width: 160px;
    margin: auto;
    border-top: 1px solid rgb(255, 255, 255);
    margin-top: 40px;
    margin-bottom: 40px;
}

.section--second-text {
    font-size: 16px;
    color: rgb(255, 255, 255);
    width: 66%;
    margin: 40px auto 50px auto;
}

.section-img {
    text-align: center;
    padding-bottom: 60px;
}
</style>