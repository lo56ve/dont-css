<template>
    <div class="polygon__wrap">
        <div class="triangle"></div>
    </div>
</template>

<style scoped>
    .polygon__wrap {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        /* place-items: <align-items> / <justify-items>; */
        place-items: center / center;
    }
    .triangle {
        width: 0;
        border: 30px solid transparent;
        border-bottom-color: red;
    }
</style>

