<template>
  <div>
    <div class='recomment-title'>周末去哪</div>
    <ul>
      <li class='item' border-bottom v-for='item of recommentList' :key='item.id'>
        <div class='item-img-wrapper'>
          <img class='item-img' :src='item.imgUrl' alt>
        </div>
        <div class='item-info'>
          <p class='item-title'>{{item.title}}</p>
          <p class='item-desc'>{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data() {
    return {
      recommentList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/87/b46b43303b585c.jpg_r_640x214_af2aa659.jpg',
          title: '鸟巢',
          desc: '2018年北京奥运会主会场'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/87/b46b43303b585c.jpg_r_640x214_af2aa659.jpg',
          title: '鸟巢',
          desc: '2018年北京奥运会主会场'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/87/b46b43303b585c.jpg_r_640x214_af2aa659.jpg',
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
}

.item-img-wrapper{
    overflow :hidden;
    height :0;
    padding-bottom :33.9%;
}

.item-img {
  width :100%;
}

.item.info {
  padding: 0.1rem;
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

</style>
