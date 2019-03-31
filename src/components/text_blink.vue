<template>
    <div>
        <div class="smooth-blink">平滑闪烁文本</div>
        <div class="normal-blink">普通闪烁文本</div>
    </div>
</template>

<style scoped>
    @keyframes smooth-blink {
        to {color: transparent;}
    }
    .smooth-blink {
        animation: .5s smooth-blink 6 alternate;
    }

    @keyframes blink {
        50% {
            color: transparent;
        }
    }
    /* 1s：每个动画执行时长
        blink：执行动画
        6：动画播放的次数
        steps(1)：等同于steps(1, end)，表示当前颜色与transparent之间的过度会在一次步进中完成 */
    .normal-blink {
        animation: blink 1s 6 steps(1);
    }
</style>

