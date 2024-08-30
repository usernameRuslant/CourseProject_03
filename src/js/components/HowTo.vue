<template>
  <div>
    <h2 class="howto__title">Не знаете с чего начать?</h2>
    <p>
      Программы предлагают ежедневные рекомендации в интерактивном календаре
    </p>
    <div class="blocks" :style="'left: ' + left + 'px'">
      <div class="item">
        <h3>Видео тренировки 1</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 2</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 3</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 4</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 5</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 6</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировки 7</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        <i class="fas fa-arrow-right"></i>
      </div>
    </div>
    <div class="arrows">
      <img
        src="/img/arrow.svg"
        v-if="this.left != 0"
        @click="moveBlock('prev')"
        alt=""
      />
      <img
        src="/img/arrow.svg"
        class="next"
        v-if="this.left >= -1600"
        @click="moveBlock('next')"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      left: 0,
    };
  },
  methods: {
    moveBlock(value) {
      let add = 320;
      console.log(this.left);
      if (value == 'next' && this.left >= -1600) this.left -= add;
      else if (value == 'prev' && this.left != 0) this.left += add;
    },
  },
};
</script>

<style lang="scss" scoped>
.howto__title {
  margin-top: 80px;
  font-size: 2.4em;
}
p {
  color: #9b9a97;
  margin-top: 15px;
}
.blocks {
  display: flex;
  margin-top: 35px;
  margin-bottom: 17px;
  width: 2500px;
  position: relative;
  transition: left 500ms ease;

  .item {
    background: #323443;
    padding: 30px 25px;
    border-radius: 12px;
    width: 250px;

    &:not(:last-of-type) {
      margin-right: 25px;
    }
    p {
      color: #9b9a97;
    }
    i {
      float: right;
      font-size: 1.2em;
      position: relative;
      bottom: 25px;
    }
  }
}

.arrows {
  margin-bottom: 130px;
  img {
    cursor: pointer;
    transition: transform 500ms ease;
    margin-right: 30px;

    &:hover {
      transform: scale(1.1);
    }
    &.next {
      transform: rotate(180deg);
      &:hover {
        transform: scale(1.1) rotate(180deg);
      }
    }
  }
}
</style>
