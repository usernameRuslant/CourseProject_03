<template>
  <div>
    <div class="features">
      <div class="features__heading">
        <img src="/img/yellowLine.svg" alt="yellow" />
        <h3>Тренировки Специально Для тебя</h3>
      </div>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua consectetur
        adipiscing.
      </p>
      <button>Начать</button>
    </div>
    <div class="pictures">
      <div>
        <img src="img/tren1.png" alt="tren1" />
        <h4>Саманта Вильям</h4>
        <p>Тренер</p>
      </div>
      <div class="mid">
        <img src="img/tren2.png" alt="tren2" />
        <h4>Алина Реймонд</h4>
        <p>Тренер</p>
      </div>
      <div>
        <img src="img/tren3.png" alt="tren3" />
        <h4>Джонатан Вайз</h4>
        <p>Тренер</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {},
};
</script>

<style lang="scss" scoped>
.features {
  width: 1500px;

  background: #191919;
  position: relative;

  @media (min-width: 1380px) {
    margin-left: 391px;
  }
  @media (max-width: 1380px) and (min-width: 1100px) {
    margin-left: 191px;
  }
  @media (min-width: 1100px) {
    padding: 130px 120px 400px 320px;
  }
  @media (max-width: 1100px) {
    padding: 50px;
  }
  p {
    color: #ababab;

    line-height: 200%;

    // @media (min-width: 1100px) {
    //   font-size: 1em;
    //   width: 600px;
    // }

    @media (min-width: 560px) {
      font-size: 1.5em;
      width: 460px;
    }
    @media (max-width: 560px) {
      font-size: 1.05em;
      width: 250px;
    }
  }
  button {
    background: #25ab75;
    padding: 20px;
    width: 160px;
    font-weight: 600;
    font-size: 1.02em;
    color: #fff;
    border: 0;
    cursor: pointer;
    border-radius: 10px;
    margin-top: 30px;
    transition: transform 500ms ease;

    &:hover {
      transform: translateY(-7px);
    }
  }
  .features__heading {
    @media (min-width: 1100px) {
      position: absolute;
      top: 0px;
      left: -230px;
    }

    h3 {
      
      @media (min-width: 1100px) {
        position: relative;
        top: -24px;
        left: -66px;
      }


      @media (min-width: 560px) {
        font-size: 4.5em;
        width: 560px;
        font-weight: 600;
        line-height: 133%;
      }
      @media (max-width: 560px) {
        font-size: 2.3em;
        width: 300px;
        font-weight: 600;
        line-height: 133%;
      }
    }
    img {
      @media (min-width: 1100px) {
        position: relative;
        top: 439px;
        left: -121px;
      }
    }
  }
}
.pictures {
  margin-bottom: 100px;
  display: flex;

  @media (min-width: 1380px) {
    padding-left: 70px;
  }
  @media (max-width: 1380px) and (min-width:1100px){
    position: relative;
    left: -130px;
  }
  @media (max-width: 1100px) {
    flex-wrap: wrap;
    justify-content: space-between;
  }

  > div {
    @media (min-width: 1100px) {
    position: relative;
    
  }
  @media (max-width: 1100px) {
    margin-top: 100px;
    
  }
    
    &.mid {
      top: 321px;
    }
    &:last-of-type {
      top: -193px;

      h4,
      p {
        padding-left: 25px;
      }
    }
    h4 {
      margin-top: 20px;
      font-weight: 500;
      font-size: 1.3em;
    }
    p {
      font-size: 0.9em;
      color: #ababab;
      font-weight: 400;
    }
  }
}
</style>
