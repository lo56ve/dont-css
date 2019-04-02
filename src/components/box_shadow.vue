<template>
    <div class="shadow__wrap">
        <div class="shadow__box1">非线性阴影1</div>
        <div class="shadow__box2">非线性阴影2</div>
    </div>
</template>

<style scoped>
    .shadow__wrap {
        display: grid;
        height: calc(100% - 40px);
        grid-template-rows: 1fr 1fr;
        justify-content: center;
        align-items: center;
    }
    .shadow__box1 {
        width: 100px;
        color: white;
        line-height: 40px;
        text-align: center;
        height: 40px;
        background: linear-gradient(to right, #53a8ff, #123a63);
        border-radius: 10px;
        /* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影扩散半径(相当于每个方向偏移量) | 阴影颜色 */
        box-shadow: -10px 0 10px -8px #123a63, 10px 0 10px -8px #123a63;
    }
    .shadow__box2 {
        width: 100px;
        height: 40px;
        color: white;
        line-height: 40px;
        text-align: center;
        border-radius: 10px;
        background: linear-gradient(to right, #53a8ff, #123a63);
        box-shadow: 0 10px 4px -8px black;
    }
</style>

