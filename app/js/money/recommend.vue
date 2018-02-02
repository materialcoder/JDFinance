<template lang="html">
    <Panel :class="$style.panel" title="精选推荐">
        <section :class="$style.content">
            <dl :class="$style.item" v-for="item in items" :key="item.title">
                <dt>{{item.title}}<span>{{item.sub}}</span></dt>
                <dd>{{item.rate}}</dd>
                <dd>{{item.text}}</dd>
            </dl>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel";
export default {
  components: {
    Panel
  },
  data() {
    return {
      items: [
        {
          title: "定期理财",
          sub: "90天可质押",
          rate: "5.50%",
          text: "历史年化结算利率"
        },
        {
          title: "固收理财",
          sub: "理财首选",
          rate: "5.80%",
          text: "综合年化收益率"
        },
        {
          title: "基智账户",
          sub: "组合投资",
          rate: "8%-10%",
          text: "止盈年化收益率"
        },
        {
          title: "小白基金",
          sub: "天天赚钱",
          rate: "4.27%",
          text: "7日年化收益率"
        }
      ]
    };
  }
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .content {
    @include flex(row);
    box-sizing: border-box;
    &:after {
      content: "";
      display: block;
      width: 100%;
      height: 0;
      border-bottom: 1px solid #ddd;
      position: relative;
      top: -219px;
    }
    .item {
      width: 50%;
      height: 218px;
      box-sizing: border-box;
      padding-left: 32px;
      padding-top: 34px;
      position: relative;
      &:after {
        content: "";
        display: block;
        width: 1px;
        height: 136px;
        position: absolute;
        top: 50%;
        right: 0;
        margin-top: -68px;
        border-right: 1px solid #ddd;
      }
      &:nth-child(2n) {
        &:after {
          display: none;
        }
      }
      dt {
        font-size: 30px;
        line-height: 42px;
        color: #333;
        font-weight: 700;
        span {
          font-size: 24px;
          color: #ff5155;
          border: 1px solid #ff5155;
          padding: 0 8px;
          margin-left: 2px;
          vertical-align: 1px;
        }
      }
      dd {
        &:nth-child(2) {
          font-size: 44px;
          font-weight: 700;
          color: #ff5155;
          height: 58px;
          line-height: 58px;
        }
        &:nth-child(3) {
          font-size: 24px;
          color: #999;
          height: 34px;
          line-height: 34px;
          text-overflow: ellipsis;
          white-space: nowrap;
          overflow: hidden;
        }
      }
    }
  }
}
</style>