<template>
    <div class="menu-wrap">

         <table
         class="spreadsheet-wrapper">

         <tr>
            <td
            v-for="item in items"
            :key="item.id"
            class="spreadsheet-column">

            <a class="menu-link">{{ item.value }}</a></td>
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
.menu-wrap {
    display: flex;
    justify-content: space-between;
}

.spreadsheet-wrapper {
    border-collapse: collapse;
}

.spreadsheet-column {
    text-align: center;
    width: 1110px;
    border: 1px solid rgb(255, 255, 255);
    border-left-width: 0;
    height: 47px;
}

.spreadsheet-column:last-child {
    border-right-width: 0;
}
.menu-link {
    cursor: pointer;
}
</style>