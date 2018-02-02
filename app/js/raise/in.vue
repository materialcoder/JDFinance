<template lang="html">
    <Panel :class="$style.panel" title="In货推荐">
        <section :class="$style.content">
            <div :class="$style.item" v-for="item in items" :key="item.catgory">
                <img :src="item.catgory" alt="">
                <section :class="$style.list">
                    <div :class="$style.product" v-for="product in item.list" :key="product.img">
                        <img :src="product.img" alt="">
                        <h4 :class="$style.title">{{product.title}}</h4>
                        <p :class="$style.price"><em>{{product.price}}</em>起</p>
                        <article v-if="!product.end">
                            <div :class="$style.wrapper">
                                <div :class="$style.inner" :style="{width: product.progress+'%'}"></div>
                            </div>
                            <p>{{product.progress}}%</p>
                        </article>
                        <div v-if="product.end" :class="$style.end">众筹结束</div>
                        <label v-if="product.special">精选</label>
                    </div>
                </section>
            </div>
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
          catgory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200",
          list: [
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t16150/165/674827881/130789/7de1f069/5a3a04b0N4e3d246c.jpg",
              title: "骨传导耳机",
              price: "19.00",
              progress: 388,
              special: true,
              end: false
            },
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t15514/150/953212838/145464/850c2d0f/5a448bc7Nade1a7c5.jpg",
              title: "未来游戏装备",
              price: "159.00",
              progress: 40,
              special: false,
              end: true
            }
          ]
        },
        {
          catgory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200",
          list: [
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.jpg",
              title: "蓝牙音箱",
              price: "29.00",
              progress: 40,
              special: false,
              end: true
            },
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t14767/339/1285461444/50279/8ee27acb/5a4c3a82N3cff563e.jpg",
              title: "全球漫游WiFi卡",
              price: "65.00",
              progress: 359,
              special: false,
              end: false
            }
          ]
        },
        {
          catgory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3214/113/4408032436/61548/ce316eef/5846d310Ne93f00c9.png?width=750&height=200",
          list: [
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t8245/192/196081959/46158/74227a9a/59a26d4bNddd40149.jpg",
              title: "遵义虾子土豆片",
              price: "1.00",
              progress: 0,
              special: false,
              end: false
            },
            {
              img:
                "//img30.360buyimg.com/cf/s250x250_jfs/t10993/26/1955036662/116896/13538743/59ec19ecN5efa5c7d.jpg",
              title: "新疆黄杏干",
              price: "35.00",
              progress: 0,
              special: false,
              end: false
            }
          ]
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
    @include flex;
    .item {
      margin-bottom: 40px;
      > img {
        display: block;
        width: 100%;
        height: 170px;
      }
      .list {
        @include flex(row);
        .product {
          width: 50%;
          height: 396px;
          box-sizing: border-box;
          text-align: center;
          position: relative;
          img {
            width: 180px;
            height: 180px;
            margin: 44px auto 20px;
          }
          .title {
            font-size: 28px;
            color: #444;
            font-weight: 700;
          }
          .price {
            font-size: 20px;
            color: #999;
            line-height: 48px;
            margin-bottom: 16px;
            em {
              color: #ff3232;
              font-size: 36px;
              font-weight: 700;
              margin-right: 4px;
              &:before {
                content: "￥";
                font-size: 28px;
                font-weight: normal;
              }
            }
          }
          article {
            @include flex(row);
            align-items: center;
            justify-content: space-around;
            padding: 0 30px;
            .wrapper {
              width: 144px;
              height: 10px;
              background: #f6e6e6;
              border-radius: 22px;
              .inner {
                width: 80%;
                max-width: 100%;
                height: 10px;
                background-image: linear-gradient(
                  270deg,
                  #f55 1%,
                  #ff9c31 100%
                );
                border-radius: 22px;
              }
            }
            p {
              font-size: 24px;
              color: #999;
            }
          }
          .end {
            font-size: 24px;
            height: 48px;
            line-height: 48px;
            color: #999;
            background: rgb(237, 237, 237);
            margin: 0 20px;
          }
          label {
            position: absolute;
            top: 0;
            left: 20px;
            font-size: 24px;
            color: #f00;
            text-align: center;
            padding: 4px 8px;
            background: linear-gradient(-35deg, #c1c1c1 0, #acacac 100%);
          }
        }
      }
    }
  }
}
</style>