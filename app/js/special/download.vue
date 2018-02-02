<template lang="html">
    <Panel title="下载APP" :class="$style.panel">
        <section :class="$style.content">
            <div></div>
            <p>立即下载</p>
            <span>Copyright</span>
        </section>
    </Panel>
</template>

<script>
import Panel from '../core/panel'
    export default {
        components: {
            Panel
        }
    }
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    margin: 0;
    background: #fff;
    > h4 {
        display: none;
    }
    .content {
        @include flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 1136px;
        >div {
            background: url(//img12.360buyimg.com/jrpmobile/jfs/t8956/285/1249806938/50853/8cd3c8f0/59b65f36N05367075.png) center center no-repeat;
            width: 600px;
            height: 800px;
            background-size: 100% auto;
            margin-top: -400px;
        }
        >p{
            @include btn($size:32px, $color:#fff, $bgcolor:#f1443e, $padding:0, $radius:10px);
            height: 100px;
            line-height: 100px;
            width: 471px;
            background-image: linear-gradient(278deg, #f55c33 0, #ee2d18 75%);
            box-shadow: 0 12px 32px 0 rgba(255, 159, 135, .6);
            position: fixed;
            bottom: 130px;
        }
        span {
            position: fixed;
            bottom: 16px;
            font-size: 20px;
            color: #eee;
        }
    }
}
</style>