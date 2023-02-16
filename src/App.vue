<template>
  <div class="wrapper">
    <div class="content"></div>
    <span class="title">活期理财</span>
    <van-button type="primary">主要按钮</van-button>
    <van-empty description="描述文字" />
    <van-card
      num="2"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
    />
    <div class="box">
      <div class="aspect">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dignissimos
        quia deserunt aliquid perferendis voluptatum enim! Tempore, ab adipisci
        ex minus nobis corporis autem vero minima perspiciatis asperiores,
        repellendus odio consequatur.
      </div>
    </div>
    <div class="s_wrapper">
      <div class="item_wrapper">
        <div class="s_item">123</div>
        <div class="s_item">456</div>
        <div class="s_item">789</div>
        <div class="s_item">101112</div>
        <div class="s_item">131415</div>
      </div>
    </div>
  </div>
</template>

<script>
import _ from "lodash";
import image from "./test.webp";
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      nextNum: 10,
      image,
    };
  },
  mounted() {
    // this.ob();
  },
  methods: {
    shuffle: function () {
      this.items = _.shuffle(this.items);
    },
    randomIndex: function () {
      return Math.floor(Math.random() * this.items.length);
    },
    add: function () {
      this.items.splice(this.randomIndex(), 0, this.nextNum++);
    },
    remove: function () {
      this.items.splice(this.randomIndex(), 1);
    },
    // ob() {
    //   const cb = (mutationsList) => {
    //     console.log(mutationsList);
    //   };
    //   const ob = new MutationObserver(cb);
    //   ob.observe(document.querySelector(".target"), {
    //     childList: true,
    //     attributes: true,
    //   });
    //   console.log(document.querySelector(".target"));
    // },
  },
};
</script>
<style scoped>
.s_wrapper {
  overflow: hidden;
}
.item_wrapper {
  display: flex;
  height: 100px;
  width: 100%;
  position: relative;
}
.s_item {
  flex-basis: 60%;
  flex-grow: 0;
  flex-shrink: 0;
  border: 1px solid red;
}
.box {
  width: 50%;
  margin: auto;
}
.aspect {
  background: orange;
  padding-top: 75%;
}
.container {
  height: 100px;
}
/* .box {
  padding-top: 100%;
  width: 50%;
} */
.item {
  background-color: aquamarine;
}
.list-item {
  display: inline-block;
  margin-right: 10px;
  transition: all 1s;
}
.list-enter,
.list-leave-to {
  transform: translateY(40px);
}
/* .list-leave-active {
  position: absolute;
} */
/* .list-enter-active {
  
} */
</style>

<style scoped>
.title {
  font-size: 15px;
  font-family: PingFangSC-Semibold, PingFang SC;
  font-weight: 600;
  color: rgba(0, 0, 0, 0.9);
  line-height: 21px;
}
.wrapper {
  padding: 14px;
}
.content {
  width: 347px;
  height: 112px;
  box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.12);
  border-radius: 8px;
  border: 1px solid red;
}
</style>
<style>
html,
body {
  padding: 0;
  margin: 0;
}
</style>
