<template>
  <div>
    <div class="heading">
      <h2 class="courses__title">Популярные Тренировки</h2>
      <a href="#">ПОСМОТРЕТЬ БОЛЬШЕ</a>
    </div>
    <div class="courses">
      <div class="courses__item" v-for="el in courses" :key="el.title">
        <img :src="'/img/' + el.img" :alt="el.title" />
        <h2>{{ el.title }}</h2>
        <p>{{ el.cl }}</p>
        <div class="time">{{ el.time }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['data'],
  created() {
    this.courses = this.data;
  },
  data() {
    return {
      courses: [],
    };
  },
};
</script>

<style lang="scss" scoped>
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 50px;

  @media (max-width: 1024px) {
    margin-top: 70px;
  }

 .courses__title {
    font-size: 2.1em;
    

    @media (max-width: 320px) {
      font-size: 1.5em;
    }
  }

  a {
    font-size: 0.8em;
  }
}

.courses {
  margin-bottom: 250px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

  @media (min-width: 950px) {
    justify-content: space-between;
  }
  @media (max-width: 950px) {
    justify-content: center;
    flex-direction: column;
  }
  .courses__item {
    margin-top: 70px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    border-radius: 30px;

    @media (max-width: 950px) and (min-width: 425px) {
      width: 373px;
      margin-left: auto;
      margin-right: auto;
    }
    @media (max-width: 425px) {
      width: 100%;
    }
    .time {
      position: absolute;
      right: 0;
      bottom: 55px;
      background: #000;
      padding: 10px;
      font-weight: 600;
      border-top-left-radius: 15px;
    }
    h2 {
      font-size: 2.2em;
      margin-left: 20px;
      position: relative;
      bottom: 35px;
    }
    p {
      color: #ababab;
      position: relative;
      bottom: 35px;
      font-size: 0.9em;
      margin-left: 20px;
    }
    img {
      opacity: 0.8;
      transition: all 500ms ease;

      @media (max-width: 425px) {
        width: 100%;
      }

      &:hover {
        opacity: 1;
        transform: scale(1.1);
      }
    }
  }
}
</style>
