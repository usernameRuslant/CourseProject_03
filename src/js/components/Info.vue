<template>
  <div>
    <div class="blocks_b">
      <div>
        <h2>Тренируйтесь дома</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat.
        </p>
        <span><a href="#">Больше</a><i class="fas fa-arrow-right"></i></span>
      </div>
      <div>
        <img src="/img/info-1.png" alt="" />
      </div>
    </div>
    <div class="blocks_b">
      <div>
        <div>
          <img src="/img/info-2.png" alt="" />
        </div>
        <h2>
          Получите еще <br />
          больше полезного <br />
          контента
        </h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat.
        </p>
        <span><a href="#">Больше</a><i class="fas fa-arrow-right"></i></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.blocks_b {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 80px;

  @media(max-width:1100px){
    flex-direction: column;
  }
  > div {
    
    @media(min-width:900px){
      width: 50%;
  }
    h2 {
      margin-bottom: 30px;
      font-size: 2em;
    }
    p {
      color: #9b9a97;
      width: 450px;
      margin-bottom: 20px;
    }
    span {
      a {
        color: #0070c9;
      }
      i{
        margin-left: 15px;
        font-size: 1.2em;
      }
    }
    img {
      max-width: 90%;

      @media(max-width:1100px){
    &:first-of-type{margin-top: 20px;}
  }
    }
  }
}
</style>
