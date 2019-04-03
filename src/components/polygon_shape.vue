<template>
    <div class="polygon__wrap">
        <div class="triangle"></div>
        <div class="parallelogram1">平行四边形1</div>
        <div class="parallelogram2__wrap">
            <div class="parallelogram2__inner">平行四边形2</div>
        </div>
        <div class="pentagon"></div>
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
        border: 40px solid transparent;
        border-bottom-color: red;
        /* 由于上边框会占用30px，需要重置回去 */
        margin-top: -40px;
    }

    /* 简单的平行四边形可以直接使用skew来解决，但是保证内部的字体正常显示，需要多做以下处理 */
    .parallelogram1 {
        position: relative;
        display: inline-block;
        width: 100px;
        height: 40px;
        color: white;
        line-height: 40px;
        text-align: center;
    }
    .parallelogram1::before {
        display: inline-block;
        content: '';
        position: absolute;
        left: 0;
        top: 0;
        bottom: 0;
        right: 0;
        background-color: red;
        z-index: -1;
        transform: skewX(45deg);
    }
    
    .parallelogram2__wrap {
        height: 40px;
        width: 100px;
        color: white;
        line-height: 40px;
        text-align: center;
        background-color: red;
        transform: skewX(45deg);
    } 
    .parallelogram2__inner {
        /* 抵消原来的字体倾斜效果 */
        transform: skewX(-45deg);
    }
</style>

