<template>
    <div>
        <footer class="footer">
            <div class="content-container">
                
                <table
                class="footer-menu" >
                <tr>
                    <td
                    v-for="item in itemsMenu"
                    :key="item.id"
                    class="spreadsheet-column">

                    <a class="menu-link">{{ item.value }}</a></td>
                </tr>
                </table>

                <table
                class="footer-menu">
                <tr>
                    <td
                    class="spreadsheet-column spreadsheet-column_under">
                    винный бутик LE CORTE</td>

                    <td
                    class="spreadsheet-column spreadsheet-column_under">
                    8 (812) 123-45-67</td>

                    <td
                    class="spreadsheet-column spreadsheet-column_under icon-wrap">
                        <a class="menu-link"><img src="../../icons/VectorLeft.svg"></a>
                        <a class="menu-link"><img src="../../icons/VectorCenter.svg"></a>
                        <a class="menu-link"><img src="../../icons/VectorRight.svg"></a>
                    </td>

                    <td
                    class="spreadsheet-column spreadsheet-column_under">
                    © le-corte.ru</td>
                </tr>
                </table>

            </div>
        </footer>
    </div>
</template>

<script setup>

import { ref } from 'vue'

const itemsMenu = ref([
  { id: 1, value: 'Главная' },
  { id: 2, value: 'Каталог' },
  { id: 3, value: 'Поставщики' },
  { id: 4, value: 'Коллекции' },
  { id: 5, value: 'Дегустация' },
  { id: 6, value: 'Коллекция 2020' },
  { id: 7, value: 'Контакты' },
])

</script>

<style scoped>

.footer {
    background: #998431;
    display: flex;
    min-height: 220px;
    color: #ffffff;
    flex-direction: column;
    justify-content: center;
}

.content-container {
    width: 86%;
    margin: 0 auto;
}

.footer-menu {
    font-family: 'Montserrat';
    font-size: 14px;
    line-height: 21px;
    text-align: center;
    height: 60px;
    border-collapse: collapse;
}

.spreadsheet-column {
    text-align: center;
    width: 1110px;
    border: 1px solid #ffffff;
    border-left-width: 0;
    border-right-width: 0;
    white-space: nowrap;
}

.spreadsheet-column:first-child {
    padding-left: 60px;
}

.spreadsheet-column:last-child {
    padding-right: 60px;
}

.menu-link {
    cursor: pointer;
}

.spreadsheet-column_under {
    border-top: 0;
    border-right: 1px solid #ffffff;
    text-transform: uppercase;
    white-space: nowrap;
}

.spreadsheet-column_under:last-child {
    border-right-width: 0;
}

.spreadsheet-column_under:nth-child(2) {
    width: 25%;
}

.icon-wrap  > .menu-link:nth-child(1) {
    margin-right: 36px;
}

.icon-wrap  > .menu-link:nth-child(2) {
    margin-right: 42px;
}

.icon-wrap {
    padding: 0px 30px;
}
</style>