<template>
  <div class="container">
    <ul class="product-list">
      <li class="product-item" v-for="(item) in list" :key="item.id">
        <img :data-src="item.tupian" class="lazy">
        <div class="name">{{ item.mingzi }}</div>
        <div class="price">
          <span style="font-size: 12px;">￥</span>{{  item.jiage }}
        </div>
      </li>
    </ul>
    <img src="../assets/imgs/1000双色沙拉碗（含PP盖）.jpg" class="tt" alt="">
  </div>
</template>

<script>
import productList from '../assets/pro.json';
export default {
  name: 'ProductList',
  data() {
    return {
      list: [],
      lazyloadThrottleTimeout: null,
      lazyloadImgs: []
    }
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      this.initList();
    },
    initList() {
      this.list = productList.map(item => {
        let filename = item.mingzi.replaceAll('*', 'x').replaceAll('/', 'x');
        item.jiage = (item.jiage / 100 + item.jiage % 100 / 100).toFixed(2);
        item.tupian = require(`../assets/imgs/${filename}${item.ext}`);
        return item;
      })
      // 产品列表数据更新后再进行监听
      this.$nextTick(() => {
        this.initLazyload();
      })
    },
    initLazyload() {
      if('IntersectionObserver' in window) {
        const lazyloadImgs = document.querySelectorAll('.lazy');
        const intersectionObserver = new IntersectionObserver((entries) => {
          // 如果 intersectionRatio 为 0，则目标在视野外，
          // 我们不需要做任何事情。
          entries.forEach(entry => {
            if(entry.intersectionRatio) {
              let image = entry.target;
              image.src = image.dataset.src;
              image.classList.remove('lazy');
              // 取消监听
              intersectionObserver.unobserve(image);
            }
          })
        })

        lazyloadImgs.forEach(img => {
          intersectionObserver.observe(img);
        });
      } else {
        this.lazyloadImgs = document.querySelectorAll('.lazy');
        // 滚动
        document.addEventListener("scroll", this.lazyload);
        // 设备纵横比发生变化
        window.addEventListener("orientationChange", this.lazyload);
      }
    },
    lazyload() {
      this.lazyloadImgs.forEach((img) => {
        if (this.isInViewPort(img)) {
          img.src = img.dataset.src;
          img.classList.remove('lazy');
        }
      });
      if (this.lazyloadImgs.length == 0) {
        document.removeEventListener("scroll", this.lazyload);
        window.removeEventListener("orientationChange", this.lazyload);
      }
    },
    isInViewPort(element) {
      const viewHeight = window.innerHeight || document.documentElement.clientHeight;
      const { top, left } = element.getBoundingClientRect();
      // 这个是判断元素刚进入视口
      return (
        top >= 0 &&
        top <= viewHeight &&
        left >= 0
      );
    }
  },
}
</script>

<style scoped>
.product-list {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.product-item {
  width: 41.5%;
  padding: 2%;
  margin: 2%;
  border: 1px solid #ccc;
  border-radius: 8px;
}

img {
  width: 100%;
  height: 180px;
}

.name {
  font-size: 14px;
  width: 100%;
  height: 40px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}

.price {
  color: red;
}</style>
