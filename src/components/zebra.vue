<template>
    <div>
        <ul class="zebra__ul">
            <li class="zebra__li">斑马线第一行li元素</li>
            <li class="zebra__li">斑马线第二行li元素</li>
            <li class="zebra__li">斑马线第三行li元素</li>
            <li class="zebra__li">斑马线第四行li元素</li>
        </ul>
        <div class="zebra__div">
            斑马线斑马线斑马线斑马线同个标签内第一行文本
            斑马线斑马线斑马线斑马线同个标签内第二行文本
            斑马线斑马线斑马线斑马线同个标签内第三行文本
            斑马线斑马线斑马线斑马线同个标签内第四行文本
        </div>
    </div>
</template>

<style scoped>
    .zebra__ul {
        list-style: none;
    }
    /* odd：奇数，同2n+1
    even：偶数，同2n */
    .zebra__li:nth-child(odd){
        background-color: #ddd;
    }

    /*文本斑马线，将两行文本使用一个渐变背景*/
    .zebra__div {
        line-height: 1.5em;
        background-size: auto 3em;
        /*背景图像相对于内容框来定位*/
        /*如果有padding，以padding-box定位会有问题*/
        background-origin: content-box;
        background-image: linear-gradient(transparent 50%, #ddd 0);
    }
</style>

