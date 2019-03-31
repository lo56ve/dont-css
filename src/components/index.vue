<template>
    <div class="overview">
        <div v-for="(item, index) in componentList"
            :key="index"
            class="component__item"
            :style="{border: `1px solid ${colorList[index]}`}">
            <div class="component__item-title"
                :style="{backgroundColor: colorList[index]}"
                v-html="componentNameList.get(item)">
            </div>
            <components :is="item"></components>
        </div>
    </div>
</template>


<script>
    import { colorList, componentNameList } from './const.js';
    import TextBlink from './text_blink';
    import Zebra from './zebra';

    export default {
        components: {
            TextBlink,
            Zebra
        },

        data () {
            return {
                componentList: []
            }
        },

        computed: {
            colorList () {
                return colorList;
            },

            componentNameList () {
                return componentNameList;
            }
        },

        mounted () {
            this.componentList = Object.keys(this.$options.components);
        }
    }
</script>

<style scoped>
    .overview {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-template-rows: minmax(100px, auto);
        grid-gap: 20px;
    }

    .component__item-title {
        height: 40px;
        text-align: center;
        line-height: 40px;
    }
</style>

