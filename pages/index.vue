<template>
  <div class="app">

    <div class="flex p-2" v-gsap.fromTo="[
              {  scale: 0 },
              {  scale: 1, duration: 1,delay:1 }
            ]">Logo</div>
    <div class="container">
      <div class="row align-items-center  middle">

        <div class="col m-2">
          <div class="vertical-lr align-self-center text-center" v-gsap.fromTo="[
              {  scale: 0 },
              {  scale: 1, duration: 1,delay:1 }
            ]">О нас</div>
        </div>
        <!-- <div class="col burger ">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div> -->
        <div class="col">
          <div class="flex flex-row justify-content-center">
            <div class="flex-column align-self-center" 
            v-gsap.fromTo="[
              { opacity: 0, x: -50, scale: 0 },
              { opacity: 1, x: 0,  scale: 1, duration: 1 }
            ]">

              <span class="text">S</span><span class="text">P</span><span class="text">B</span>
            </div>

            <div class="flex-column align-self-center  " 
            v-gsap.fromTo="[
              { opacity: 0, y: -50, scale: 1 },
              { opacity: 1, y: 0,  scale: 1, duration: 1 }
            ]">
              <div class="text1">S</div>
              <div class="text1">I</div>
              <div class="text1">T</div>
              <div class="text1">E</div>
            </div>
          </div>
        </div>
        <div class="col catalog">
          <div class="lines"
          v-gsap.fromTo="[
              {  y: -1000 },
              {  y: 0, duration: 1 }
            ]" ></div>
          <div class="catalog_text"
          v-gsap.fromTo="[
              {  scale: 0 },
              {  scale: 1, duration: 1,delay:1 }
            ]"
          >Каталог</div>
          <div class="lines"
          v-gsap.fromTo="[
              {  y: 1000 },
              {  y: 0, duration: 1 }
            ]"
          ></div>
        </div>
        <div class=" col flex justify-content-end m-4">
          <div class="vertical-lr"  v-gsap.fromTo="[
              {  scale: 0 },
              {  scale: 1, duration: 1,delay:1 }
            ]">Контакты</div>
        </div>
      </div>
    </div>
    <footer class="flex footer" style="font-size:1rem"  v-gsap.fromTo="[
              {  scale: 0 },
              {  scale: 1, duration: 1,delay:1 }
            ]">
       SpbSite(c)
    </footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style scoped>
.container {
  width: 100%;
  padding-right: var(--bs-gutter-x, 0.75rem);
  padding-left: var(--bs-gutter-x, 0.75rem);
  margin-right: auto;
  margin-left: auto;
}

.row {
  --bs-gutter-x: 1.5rem;
  --bs-gutter-y: 0;
  display: flex;
  flex-wrap: wrap;
  margin-top: calc(var(--bs-gutter-y) * -1);
  margin-right: calc(var(--bs-gutter-x) * -.5);
  margin-left: calc(var(--bs-gutter-x) * -.5);
}

.row>* {
  box-sizing: border-box;
  flex-shrink: 0;
  width: 100%;
  max-width: 100%;
  padding-right: calc(var(--bs-gutter-x) * .5);
  padding-left: calc(var(--bs-gutter-x) * .5);
  margin-top: var(--bs-gutter-y);
}

.align-items-center {
  align-items: center !important;
}

.col {
  flex: 1 0 0%;
}

.footer{
  width: 100vw;
  position: absolute;
  bottom:10px;
 
}

.app {
  padding: 0;
  margin: 0;
  width: 100vw;
  height: 100vh;
  background-color: black;
  color: white
}

.middle {
  margin-top: 37vh;
  height: 20vh
}

.line {
  width: 50px;
  height: 1px;
  margin-bottom: 10px;
  background-color: white;
}

.text-center {
  text-align: center;
}

.lines {
  width: 1px;
  height: 50px;

  margin: 15px auto;
  background-color: white;
}
.catalog_text {
    text-align: center;
  }
.container{
  padding: 0;
}
.middle{
  margin: 0;
  margin-top: 35vh;
  height: 20vh;
}
@media (max-width: 700px) {
  .burger {
    position: absolute;
    top: 20px;
    left: 85vw;
  }

  .catalog {
    position: absolute;
    top: 100px;
  }
  

}
</style>