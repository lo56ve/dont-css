<template>
    <div class="shadow__wrap">
        <div class="shadow__box">
            非线性阴影
        </div>
    </div>
</template>

<style scoped>
    .shadow__wrap {
        display: flex;
        height: 100%;
        width: 100%;
        align-items: center;
        justify-content: center;
    }
    .shadow__box {
        width: 100px;
        color: white;
        line-height: 40px;
        text-align: center;
        height: 40px;
        background: linear-gradient(to right, #53a8ff, #123a63);
        border-radius: 10px;
        /* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影扩散半径 | 阴影颜色 */
        box-shadow: 10px 0 10px -5px #123a63, -10px 0 10px -5px #123a63;
    }
</style>

