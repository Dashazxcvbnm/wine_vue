<template>
    <div>

         <table
         class="spreadsheet-wrapper">

         <tr 
         class="table-row"
         v-for="item in items"
         :key="item.id">

            <td class="table-column">{{ item.age }}</td>

            <td class="table-column">
                <h2 class="subtitle">{{ item.subtitle }}</h2>
                <div class="text">{{ item.text }}</div>
            </td>

         </tr>
         </table>
    </div>
</template>

<script setup>

defineProps({
    items: {
        type: Array
    }
})

</script>

<style scoped>

.spreadsheet-wrapper {
    border-collapse: collapse;
    margin-bottom: 30px;
}

.table-row {
    border: 1px solid #282828;
    border-top-width: 0;
    border-right-width: 0;
    border-left-width: 0;
}

.table-column {
    border-left: 1px solid #282828;
    white-space: nowrap;
}

.table-column:first-child {
   border-left-width: 0;
   padding: 26px 24px 26px 15px;
   font-family: 'Montserrat';
   font-size: 14px;
   line-height: 21px;
}

.table-column:last-child {
   padding: 0px 20px 17px 30px;
}

.table-row:last-child {
   border-bottom-width: 0;
}

.subtitle {
    padding-bottom: 5px;
    font-family: 'Playfair Display';
    font-size: 15px;
    line-height: 37px;
    margin: 0;
    padding: 0;
}

.text {
    font-family: 'Montserrat';
    font-size: 14px;
    line-height: 21px;
}
</style>