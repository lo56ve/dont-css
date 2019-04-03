<template>
    <div class="tab__wrap">
        <div class="tab__item">标签页A</div>
        <div class="tab__item">标签页B</div>
        <div class="tab__item">标签页C</div>
    </div>
</template>

<style scoped>
    .tab__wrap {
        text-align: center;
    }
    .tab__item {
        position: relative;
        display: inline-block;
        padding: 1em 1em 0;
        cursor: pointer;
    }
    .tab__item::before {
        content: '';
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        bottom: 0;
        z-index: -1;
        background-image: linear-gradient(hsla(0, 0%, 100%, .6), hsla(0, 0%, 100%, 0));
        transform: perspective(.5em) rotateX(5deg);
        transform-origin: bottom;	    /*在3D空间旋转时固定住底边*/
        box-shadow: 0 .15em white inset;
        border-radius: .5em .5em 0 0;
        border: 1px solid rgba(0, 0, 0, .4);
        background-color: #ccc;
        border-bottom: none;
    }
</style>

