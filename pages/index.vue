<template>
  <div class="app">

    <div class="flex p-2" v-gsap.fromTo="[
      { scale: 0 },
      { scale: 1, duration: 1, delay: 1 }
    ]">SW WEBSITE</div>
    <div class="container">
      <div class="row align-items-center  middle">

        <div class="col m-2 flex flex-row">
          <div class="line1 "></div>
          <div class="vertical-lr align-self-center text-center" v-gsap.fromTo="[
            { scale: 0 },
            { scale: 1, duration: 1, delay: 1 }
          ]">WEBSITE</div>
        </div>
        <!-- <div class="col burger ">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div> -->
        <div class="col">
          <div class="flex flex-row justify-content-center">
            <div class="flex-column align-self-center" v-gsap.fromTo="[
              { opacity: 0, x: -50, scale: 0 },
              { opacity: 1, x: 0, scale: 1, duration: 1 }
            ]">

              <span class="text">W</span><span class="text">E</span><span class="text">B</span>
            </div>

            <div class="flex-column align-self-center  " v-gsap.fromTo="[
              { opacity: 0, y: -50, scale: 1 },
              { opacity: 1, y: 0, scale: 1, duration: 1 }
            ]">
              <div class="text1">S</div>
              <div class="text1">I</div>
              <div class="text1">T</div>
              <div class="text1">E</div>
            </div>
          </div>
        </div>
        <div class="col catalog ">
          <div class="lines" v-gsap.fromTo="[
            { y: -1000 },
            { y: 0, duration: 1 }
          ]"></div>
          <div class="lines11 lines12"></div>
          <div class="lines11 lines13"></div>
          <nuxt-link to="/catalogue">
          <div class="catalog_text" v-gsap.fromTo="[
            { scale: 0 },
            { scale: 1, duration: 1, delay: 1 }
          ]" >МЫ ДЕЛАЕМ</div>
           <div class="lines11 lines22"></div>
          <div class="lines11 lines23"></div>
        </nuxt-link>

          <div class="lines" v-gsap.fromTo="[
            { y: 1000 },
            { y: 0, duration: 1 }
          ]"></div>
        </div>
        <div class=" col flex flex-row justify-content-end m-4">
          <div class="vertical-lr" v-gsap.fromTo="[
            { scale: 0 },
            { scale: 1, duration: 1, delay: 1 }
          ]">WEBSITE</div>
                  <div class="line2"></div>
        </div>
       
      

      </div>
    </div>
    <footer class="flex footer" style="font-size:1rem" v-gsap.fromTo="[
      { scale: 0 },
      { scale: 1, duration: 1, delay: 1 }
    ]">
      ® SPB-SITE
    </footer>
  </div>
</template>

<script>


export default {
  name: 'IndexPage',
  mounted() {
    this.boxRotation()
    setTimeout(()=>{
      this.change()
    },5000)
    
  },

  methods: {
    boxRotation() {
      const gsap = this.$gsap
      gsap.fromTo('.line1', {y: -1000,},{ y: 0, duration: 1 })
      gsap.fromTo('.line2', {y: 1000,},{ y: 0, duration: 1 })
      gsap.fromTo('.lines12', {width: 0,},{ width: 70, duration: 1,delay:1 })
      gsap.fromTo('.lines13', {width: 0,},{ width: 100, duration: 1,delay:1 })
      gsap.fromTo('.lines22', {width: 0,},{ width: 100, duration: 1,delay:1 })
      gsap.fromTo('.lines23', {width: 0,},{ width: 70, duration: 1,delay:1 })

    },
    telegram(){
      document.location.href = 'https://t.me/spbsite'
    },
    change(){
      const gsap = this.$gsap
      // gsap.fromTo('.app', {backgroundColor: 'black',},{ backgroundColor:'aqua', duration: 0.5 })
      // gsap.fromTo('.app', {backgroundColor: 'aqua',},{ backgroundColor:'greed', duration: 0.5,delay:0.5 })
      // gsap.fromTo('.app', {backgroundColor: 'greed',},{ backgroundColor:'black', duration: 0.5,delay:1.0 })
    }

  }

}
</script>

<style scoped>
a{
  text-decoration: none;
}
.catalog_text{
  color: white;
}
.line1 {
  position: relative;
  align-self: center;
  right: 10px;
  height: 10vh;
  width: 1px;
  background-color: #07fe64;
}

.line2 {
  position: relative;
  align-self: center;
  left: 10px;
  height: 10vh;
  width: 1px;
  background-color: aqua;
}

.lines11 {
  height: 1px;
}

.lines12 {
  width: 70px;
  margin: 15px auto;
  background-color: yellow;
}
.lines13 {
  width: 100px;
  margin: 15px auto;
  background-color: #07fe64;
}
.lines14 {
  width: 70px;
  margin: 15px auto;
  background-color: aqua;
}


.lines22 {
  width: 100px;
  margin: 15px auto;
  background-color: #07fe64;
}
.lines23 {
  width: 70px;
  margin: 15px auto;
  background-color: aqua;
}
.lines24 {
  width: 150px;
  margin: 15px auto;
  background-color: aqua;
}

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




.align-items-center {
  align-items: center !important;
}

.col {
  flex: 1 0 0%;
}

.footer {
  width: 100vw;
  position: absolute;
  bottom: 10px;

}

.app {
  font-family: "Robtronika-Regular", normal !important;
  padding: 0;
  margin: 0;
  width: 100vw;
  height: 100vh;
  background-color: black;
  color: white
}

.middle {
  /* margin-top: 46vh; */
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

.container {
  padding: 0;
}

.middle {
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

  /* .catalog {
    position: absolute;
    top: 100px;
  } */
  div.col:nth-child(2) {
 display: none;
}



}


/* Inline #5 | http://localhost:7781/cart */

#slider article  {
  
  position: absolute;
  
  bottom: 15vh;
}
.app{
  font-size: 1.5rem;
}
</style>

