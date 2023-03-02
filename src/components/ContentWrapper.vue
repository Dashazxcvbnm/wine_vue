<template>
    <div 
    class="section">
        <div 
        class="content-container">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>

.section {
    text-align: center;
    height: 100vh;
}

.content-container {
    width: 1110px;
    margin: 0 auto;
}
</style>