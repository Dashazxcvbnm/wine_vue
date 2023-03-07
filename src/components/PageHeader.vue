<template>
    <div>
        <div class="header">
        <span>Новокузнечный переулок 4/1</span>
        <span>"8 (812) 123-45-67"</span>

            </div>
                <NavigationMenu :items="items"></NavigationMenu>
            </div>
</template>

<script setup>
import NavigationMenu from './GUI/NavigationMenu.vue';

import { ref } from 'vue'

const items = ref([
  { id: 1, value: 'Каталог' },
  { id: 2, value: 'Доставка' },
  { id: 3, value: 'Коллекции' },
  { id: 4, value: 'Контакты' },
])
</script>

<style scoped>

.header {
    display: flex;
    justify-content: space-between;
    font-size: 13px;
    padding-top: 30px;
    padding-bottom: 20px;
    font-family: 'Montserrat';
    line-height: 19.5px
}
</style>