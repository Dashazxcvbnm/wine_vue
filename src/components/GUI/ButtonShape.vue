<template>
    <div>
        <button 
        class="btn">
            <slot></slot>
        </button>
    </div>
</template>

<style scoped>

.btn {
    background: rgb(153, 132, 49);
    color: rgb(255, 255, 255);
    padding: 15px 30px;
    border: none;
    font-size: 16px;
    line-height: 20px;
    font-family: 'Montserrat';
    text-transform: uppercase;
    cursor: pointer;
}
</style>