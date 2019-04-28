<template>
  <div>
    <div class='recomment-title'>热销推荐</div>
    <ul>
      <li class='item' border-bottom v-for='item of recommentList' :key='item.id'>
        <img class='item-img' :src='item.imgUrl' alt>

        <div class='item-info'>
          <p class='item-title'>{{item.title}}</p>
          <p class='item-desc'>{{item.desc}}</p>
          <button class='item-button'>查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecomment',
  data() {
    return {
      recommentList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1508/fe/434ee530e21f1c11bad088e8cc8d5e93.water.jpg_200x200_912ce9f4.jpg',
          title: '鸟巢',
          desc: '2018年北京奥运会主会场'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1508/fe/434ee530e21f1c11bad088e8cc8d5e93.water.jpg_200x200_912ce9f4.jpg',
          title: '鸟巢',
          desc: '2018年北京奥运会主会场'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1508/fe/434ee530e21f1c11bad088e8cc8d5e93.water.jpg_200x200_912ce9f4.jpg',
          title: '鸟巢',
          desc: '2018年北京奥运会主会场'
        }
      ]
    };
  }
};
</script>

<style lang='stylus' scoped>
@import '~styles/mixins.styl';

.recomment-title {
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
  margin-top: 0.2rem;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;
}

.item-img {
  width: 1.7rem;
  height: 1.7rem;
  padding: 0.1rem;
}

.item.info {
  flex: 1;
  padding: 0.1rem;
  min-width: 0;
}

.item-title {
  line-height: 0.54rem;
  font-size: 0.32rem;
  ellipsis();
}

.item-desc {
  line-height: 0.4rem;
  color: #ccc;
  ellipsis();
}

.item-button {
  background: #ff9300;
  line-height: 0.3rem;
  padding: 0.2rem;
  border-radius: 0.06rem;
  margin-top: 0.13rem;
  color: #fff;
}
</style>
