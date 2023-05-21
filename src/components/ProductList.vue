<template>
  <div class="container">
    <ul class="product-list">
      <li class="product-item" v-for="(item, index) in list" :key="index">
        <img :src="item.tupian">
        <div class="name">{{ item.mingzi }}</div>
        <div class="price">
          <span style="font-size: 12px;">￥</span>{{  item.jiage }}
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ProductList',
  data() {
    return {
      list: [
        {
          tupian: require('../assets/image001.jpg'),
          mingzi: '200碗',
          jiage:75
        },
        {
          tupian: require('../assets/image003.jpg'),
          mingzi: '200碗',
          jiage: 80
        },
        {
          tupian: require('../assets/image005.jpg'),
          mingzi: 'Y300圆碗',
          jiage: 68
        },
        {
          tupian: require('../assets/image007.jpg'),
          mingzi: 'Y300圆碗',
          jiage: 73
        },{
          tupian: require('../assets/image009.jpg'),
          mingzi: 'Y450圆碗',
          jiage: 77
        },{
          tupian: require('../assets/image011.jpg'),
          mingzi: 'Y450圆碗',
          jiage: 72
        },{
          tupian: require('../assets/image013.jpg'),
          mingzi: 'Y500圆碗',
          jiage: 88
        },{
          tupian: require('../assets/image015.jpg'),
          mingzi: 'Y500圆碗',
          jiage: 83
        },{
          tupian: require('../assets/image017.jpg'),
          mingzi: 'Y625圆碗',
          jiage: 69
        },{
          tupian: require('../assets/image019.jpg'),
          mingzi: 'Y625圆碗',
          jiage: 74
        },{
          tupian: require('../assets/image021.jpg'),
          mingzi: 'Y750圆碗',
          jiage: 77
        },{
          tupian: require('../assets/image023.jpg'),
          mingzi: 'Y750圆碗',
          jiage: 72
        },{
          tupian: require('../assets/image025.jpg'),
          mingzi: 'y800圆碗',
          jiage: 83
        },{
          tupian: require('../assets/image027.jpg'),
          mingzi: 'y800圆碗',
          jiage: 78
        },{
          tupian: require('../assets/image029.jpg'),
          mingzi: 'Y1000圆碗',
          jiage: 76
        },{
          tupian: require('../assets/image031.jpg'),
          mingzi: 'Y1000圆碗',
          jiage: 81
        },{
          tupian: require('../assets/image033.jpg'),
          mingzi: 'Y1250圆桶（平盖/高盖）',
          jiage: 72
        },{
          tupian: require('../assets/image035.jpg'),
          mingzi: 'Y1250圆桶（平盖/高盖）',
          jiage: 77
        },{
          tupian: require('../assets/image037.jpg'),
          mingzi: 'Y1500圆桶（平盖/高盖）',
          jiage: 77
        },{
          tupian: require('../assets/image039.jpg'),
          mingzi: 'Y1500圆桶（平盖/高盖）',
          jiage: 82
        },{
          tupian: require('../assets/image041.jpg'),
          mingzi: 'Y1750圆桶平盖高盖）',
          jiage: 86
        },{
          tupian: require('../assets/image043.jpg'),
          mingzi: 'Y1750圆桶平盖高盖）',
          jiage: 91
        },{
          tupian: require('../assets/image045.jpg'),
          mingzi: 'Y2000圆桶平盖/高盖）',
          jiage: 104
        },{
          tupian: require('../assets/image047.jpg'),
          mingzi: 'Y2000圆桶平盖/高盖）',
          jiage: 99
        },{
          tupian: require('../assets/image049.jpg'),
          mingzi: 'Y1250圆盆（高盖）',
          jiage: 55
        },{
          tupian: require('../assets/image051.jpg'),
          mingzi: 'Y1250圆盆（高盖）',
          jiage: 60
        },{
          tupian: require('../assets/image053.png'),
          mingzi: 'Y1500员盆（高盖）',
          jiage: 58
        },{
          tupian: require('../assets/image055.jpg'),
          mingzi: 'Y1500员盆（高盖）',
          jiage: 63
        },{
          tupian: require('../assets/image057.jpg'),
          mingzi: 'Y2000员盆（平盖/高盖）',
          jiage: 68
        },{
          tupian: require('../assets/image059.jpg'),
          mingzi: 'Y2500圆盆（平盖高盖）',
          jiage: 67
        },{
          tupian: require('../assets/image061.jpg'),
          mingzi:  'Y2500圆盆（平盖高盖） ',
          jiage: 72
        },{
          tupian: require('../assets/image063.jpg'),
          mingzi: 'Y3000圆盆（平盖/高盖）',
          jiage: 73
        },{
          tupian: require('../assets/image065.jpg'),
          mingzi: 'Y3000圆盆（平盖/高盖）',
          jiage: 78
        },{
          tupian: require('../assets/image067.jpg'),
          mingzi: 'Y3500圆盆（平盖/高盖）',
          jiage: 82
        },{
          tupian: require('../assets/image069.jpg'),
          mingzi: 'Y3500圆盆（平盖/高盖）',
          jiage: 87
        },{
          tupian: require('../assets/image071.jpg'),
          mingzi: '500方盒',
          jiage: 63
        },{
          tupian: require('../assets/image073.jpg'),
          mingzi: '500方盒',
          jiage: 55
        },{
          tupian: require('../assets/image075.jpg'),
          mingzi: 'X650方盒',
          jiage: 65
        },{
          tupian: require('../assets/image077.jpg'),
          mingzi: 'X650方盒',
          jiage: 70
        },{
          tupian: require('../assets/image079.jpg'),
          mingzi: 'X750方盒',
          jiage: 68
        },{
          tupian: require('../assets/image081.jpg'),
          mingzi: 'X750方盒',
          jiage: 73
        },{
          tupian: require('../assets/image083.jpg'),
          mingzi: 'X1000方盒',
          jiage: 79
        },{
          tupian: require('../assets/image085.jpg'),
          mingzi: 'X1000方盒',
          jiage: 74
        },{
          tupian: require('../assets/image087.jpg'),
          mingzi: '新美式750方盒',
          jiage: 61
        },{
          tupian: require('../assets/image089.jpg'),
          mingzi: '新美式1000方盒',
          jiage: 65
        },{
          tupian: require('../assets/image091.jpg'),
          mingzi: '美式700圆',
          jiage: 50
        },{
          tupian: require('../assets/image093.jpg'),
          mingzi: '美式700圆',
          jiage: 50
        },{
          tupian: require('../assets/image095.jpg'),
          mingzi: '美式900圆',
          jiage: 53
        },{
          tupian: require('../assets/image097.jpg'),
          mingzi: '美式900圆',
          jiage: 53
        },{
          tupian: require('../assets/image099.jpg'),
          mingzi: '6828美式双格',
          jiage: 100
        },{
          tupian: require('../assets/image101.jpg'),
          mingzi: '美式350圆',
          jiage: 63
        },{
          tupian: require('../assets/image103.jpg'),
          mingzi: '美式350圆',
          jiage: 63
        },{
          tupian: require('../assets/image105.jpg'),
          mingzi: '美式450圆',
          jiage: 68
        },{
          tupian: require('../assets/image107.jpg'),
          mingzi: '美式450圆',
          jiage: 68
        },{
          tupian: require('../assets/image109.png'),
          mingzi: '美式正方750',
          jiage: 95
        },{
          tupian: require('../assets/image111.png'),
          mingzi: '美式正方1000',
          jiage: 100
        },{
          tupian: require('../assets/image113.png'),
          mingzi: '350方盒',
          jiage: 65
        },{
          tupian: require('../assets/image115.jpg'),
          mingzi: '350方盒',
          jiage: 100
        },{
          tupian: require('../assets/image117.jpg'),
          mingzi: '方型四格',
          jiage: 75
        },{
          tupian: require('../assets/image119.jpg'),
          mingzi: '1060锁扣钻石疏',
          jiage: 97
        },{
          tupian: require('../assets/image121.jpg'),
          mingzi: '1260锁扣钻石碗',
          jiage: 102
        },{
          tupian: require('../assets/image123.jpg'),
          mingzi: '1560锁扣钻石碗',
          jiage: 105
        },{
          tupian: require('../assets/image125.jpg'),
          mingzi: '1760锁扣钻石碗',
          jiage: 115
        },{
          tupian: require('../assets/11.jpg'),
          mingzi: '日式520',
          jiage: 60
        },
        {
          tupian: require('../assets/22.jpg'),
          mingzi: '日式520',
          jiage: 60
        },
        {
          tupian: require('../assets/33.jpg'),
          mingzi: '日式520',
          jiage: 60
        },
        {
          tupian: require('../assets/44.jpg'),
          mingzi: '日式750',
          jiage: 65
        },
        {
          tupian: require('../assets/55.jpg'),
          mingzi: '日式750',
          jiage: 65
        },
        {
          tupian: require('../assets/66.jpg'),
          mingzi: '日式750',
          jiage: 65
        },
        {
          tupian: require('../assets/77.jpg'),
          mingzi: '日式1000',
          jiage: 73
        },
        {
          tupian: require('../assets/88.jpg'),
          mingzi: '日式1000',
          jiage: 73
        },   {
          tupian: require('../assets/99.png'),
          mingzi: '718日式银盒',
          jiage: 125
        },
        {
          tupian: require('../assets/1.png'),
          mingzi: '4安士分体酱科杯',
          jiage: 92
        }, {
          tupian: require('../assets/2.jpg'),
          mingzi: '2安士分体酱科杯',
          jiage: 88
        }, {
          tupian: require('../assets/3.png'),
          mingzi: '4安士连体酱科杯',
          jiage: 90
        }, {
          tupian: require('../assets/4.png'),
          mingzi: '2安士连体酱科杯',
          jiage: 78
        }, {
          tupian: require('../assets/4.png'),
          mingzi: '1.5安士连体酱料杯',
          jiage: 70
        }, {
          tupian: require('../assets/6.png'),
          mingzi: '1安士连体酱料杯',
          jiage: 80
        },{
          tupian: require('../assets/a.jpg'),
          mingzi: '850mi锡纸碗【含盖】',
          jiage: 370
        },{
          tupian: require('../assets/kuaizi.jpg'),
          mingzi: '舌尖四件套',
          jiage: 60
        },{
          tupian: require('../assets/kz.jpg'),
          mingzi: '招财猫四件套',
          jiage: 60
        },{
          tupian: require('../assets/nkz.jpg'),
          mingzi: '牛皮纸四件套',
          jiage: 72
        },{
          tupian: require('../assets/mss.jpg'),
          mingzi: '美式勺四件套',
          jiage: 260
        },{
          tupian: require('../assets/jgs.jpg'),
          mingzi: '金龟勺四件套',
          jiage: 130
        },{
          tupian: require('../assets/xz.png'),
          mingzi: '塑料袋',
          jiage: 10
        },{
          tupian: require('../assets/tm.jpg'),
          mingzi: '透明塑料袋',
          jiage: 9
        },{
          tupian: require('../assets/dz.jpg'),
          mingzi: '笑脸塑料袋',
          jiage: 9
        },{
          tupian: require('../assets/wf.png'),
          mingzi: '中号无纺布袋',
          jiage: 335
        },{
          tupian: require('../assets/pq.png'),
          mingzi: '小号无纺布袋',
          jiage: 470
        },{
          tupian: require('../assets/xhy.jpg'),
          mingzi: '拉拉袋',
          jiage: 13
        },{
          tupian: require('../assets/zd.png'),
          mingzi: '1234号纸袋',
          jiage: 225
        },{
          tupian: require('../assets/bz.jpg'),
          mingzi: '白皮纸',
          jiage: 75
        },{
          tupian: require('../assets/lmz.png'),
          mingzi: '热敏纸',
          jiage: 150
        },{
          tupian: require('../assets/st.jpg'),
          mingzi: '一次性手套',
          jiage: 12
        },{
          tupian: require('../assets/dst.jpg'),
          mingzi: '独立手套',
          jiage: 14
        },{
          tupian: require('../assets/55.png'),
          mingzi: '5.5竹筷',
          jiage: 39
        },{
          tupian: require('../assets/50.jpg'),
          mingzi: '5.0竹筷',
          jiage: 33
        },
        
        
        
      ]
    }
  }
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
