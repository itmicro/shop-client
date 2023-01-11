<template>
  <div class="app">
    <div class="flex p-2">Logo</div>
    <div class="flex flex-row justify-content-between middle">
      <div class="vertical-lr align-self-center text-center">О нас</div>
      <div class="align-self-center">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
      <div>
        <div class="flex flex-row">
          <div class="flex-column align-self-center m-2">
            <div>S</div>
            <div>P</div>
            <div>B</div>
          </div>

          <div class="flex-column align-self-center">
            <div>S</div>
            <div>I</div>
            <div>T</div>
            <div>E</div>
          </div>
        </div>
      </div>
      <div class="align-self-center">Каталог</div>
      <div class="vertical-rl align-self-center">Контакты</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style scoped>
.app{
  padding: 0;
  margin: 0;
  width: 100vw;
  height: 100vh;
  background-color:black;
  color:white
}
.middle{
  margin-top: 45vh;
  height: 12vh;
}
.line {
  width: 50px;
  height: 1px;
  margin-bottom: 10px;
  background-color: white;
}
.text-center{
  text-align: center;
}
</style>