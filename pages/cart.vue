<template>
    <div class="app">

        <header>
            <!-- <div class="menu"></div> -->
            <div class="logo">SPB-SITE</div>
            <!-- <div class="basket">Basket <span>2</span></div> -->
        </header>

        <section id="slider">
            <div id="canvas-holder">
                <div v-for="(item, index) in this.products.filter(function (a) {return a.category == '63bb6010e31a6de3bb3546ea' })"  :key="index">
                <img id="slider-canvas" :src=item.imageUrl style="height: 80%;margin-top: 10%;width: 80%;margin-left: 10%;opacity: 0;">
            </div>
            </div>
             

            <article>
                <div class="slide-count">
                    <span class="index">
                        <span class="next"></span>
                        <span class="current">0{{this.active+1}}</span>
                    </span>
                    <span class="line"></span>
                    <span class="total">0{{ this.length }}</span>
                </div>

                <div v-for="(item, index) in this.products.filter(function (a) {return a.category == '63bb6010e31a6de3bb3546ea' })" style="position: absolute;" :key="index"
                    class="product-card">
                    <h1 class="slide-title" style="margin-left: 0px;padding-left: 0px;font-size: 45px; ">
                        {{ item.title }}
                    </h1>

                    <div class="description">
                        <p class="next"></p>
                        <p class="current">
                            {{ item.description }}



                        </p>

                    </div>
                </div>
                <a href="#" class="btn">ЗАКАЗАТЬ</a>

                <div class="dots"></div>

                <div class="slide-nav">
                    <button data-direction="prev" @click="prev()">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 72 32.023201">
                            <defs id="defs6">
                                <clipPath id="clipPath18" clipPathUnits="userSpaceOnUse">
                                    <path id="path16" d="M 0,24.017 H 54 V 0 H 0 Z" />
                                </clipPath>
                            </defs>
                            <g transform="matrix(1.3333333,0,0,-1.3333333,0,32.0232)" id="g10">
                                <g id="g12">
                                    <g clip-path="url(#clipPath18)" id="g14">
                                        <g transform="translate(53,12.0086)" id="g20">
                                            <path id="path22"
                                                d="m 0,0 c 0,0.267 -0.11,0.522 -0.293,0.714 l -9.899,9.999 c -0.391,0.395 -1.024,0.394 -1.414,0 -0.391,-0.394 -0.391,-1.034 0,-1.428 L -3.413,1.01 H -51 c -0.552,0 -1,-0.452 -1,-1.01 0,-0.558 0.448,-1.01 1,-1.01 h 47.586 l -8.192,-8.275 c -0.391,-0.394 -0.39,-1.034 0,-1.428 0.391,-0.394 1.024,-0.394 1.414,0 l 9.899,9.999 C -0.106,-0.525 -0.003,-0.265 0,0" />
                                        </g>
                                        <g transform="translate(53,12.0086)" id="g24">
                                            <path id="path26"
                                                d="m 0,0 c 0,0.267 -0.11,0.522 -0.293,0.714 l -9.899,9.999 c -0.391,0.395 -1.024,0.394 -1.414,0 -0.391,-0.394 -0.391,-1.034 0,-1.428 L -3.413,1.01 H -51 c -0.552,0 -1,-0.452 -1,-1.01 0,-0.558 0.448,-1.01 1,-1.01 h 47.586 l -8.192,-8.275 c -0.391,-0.394 -0.39,-1.034 0,-1.428 0.391,-0.394 1.024,-0.394 1.414,0 l 9.899,9.999 C -0.106,-0.525 -0.003,-0.265 0,0 Z" />
                                        </g>
                                    </g>
                                </g>
                            </g>
                        </svg>
                    </button>
                    <button data-direction="next" @click="next()">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 72 32.023201">
                            <defs id="defs6">
                                <clipPath id="clipPath18" clipPathUnits="userSpaceOnUse">
                                    <path id="path16" d="M 0,24.017 H 54 V 0 H 0 Z" />
                                </clipPath>
                            </defs>
                            <g transform="matrix(1.3333333,0,0,-1.3333333,0,32.0232)" id="g10">
                                <g id="g12">
                                    <g clip-path="url(#clipPath18)" id="g14">
                                        <g transform="translate(53,12.0086)" id="g20">
                                            <path id="path22"
                                                d="m 0,0 c 0,0.267 -0.11,0.522 -0.293,0.714 l -9.899,9.999 c -0.391,0.395 -1.024,0.394 -1.414,0 -0.391,-0.394 -0.391,-1.034 0,-1.428 L -3.413,1.01 H -51 c -0.552,0 -1,-0.452 -1,-1.01 0,-0.558 0.448,-1.01 1,-1.01 h 47.586 l -8.192,-8.275 c -0.391,-0.394 -0.39,-1.034 0,-1.428 0.391,-0.394 1.024,-0.394 1.414,0 l 9.899,9.999 C -0.106,-0.525 -0.003,-0.265 0,0" />
                                        </g>
                                        <g transform="translate(53,12.0086)" id="g24">
                                            <path id="path26"
                                                d="m 0,0 c 0,0.267 -0.11,0.522 -0.293,0.714 l -9.899,9.999 c -0.391,0.395 -1.024,0.394 -1.414,0 -0.391,-0.394 -0.391,-1.034 0,-1.428 L -3.413,1.01 H -51 c -0.552,0 -1,-0.452 -1,-1.01 0,-0.558 0.448,-1.01 1,-1.01 h 47.586 l -8.192,-8.275 c -0.391,-0.394 -0.39,-1.034 0,-1.428 0.391,-0.394 1.024,-0.394 1.414,0 l 9.899,9.999 C -0.106,-0.525 -0.003,-0.265 0,0 Z" />
                                        </g>
                                    </g>
                                </g>
                            </g>
                        </svg>
                    </button>
                </div>
            </article>

            <!-- <div class="category">Seating</div> -->
        </section>

    </div>
</template>
<script>
import { mapGetters, mapActions } from "vuex";
export default {
    name: "cart",
    data: () => ({
        length: 0,
        active: 0,
        result:[]
    }),
    async mounted() {
        await this.fetchProducts();

        this.result = this.products.filter(function (a) {return a.category == '63bb6010e31a6de3bb3546ea' })
        console.log(this.result)
        console.log( this.result.length)
        this.length = this.result.length
        // if (this.length < 10) {
        //     this.length = '0' + this.length
        // }
        const gsap = this.$gsap
        const whole = document.querySelectorAll('.product-card')[0]
        gsap.fromTo(whole, { opacity: 0 }, { opacity: 1, duration: 1 })
        gsap.fromTo('img', { opacity: 0,x:-100,scaleY:0 }, {x:0,scaleY:1, opacity: 1, duration: 1,delay:1 })
    },
    computed: {
        ...mapGetters({
            products: "products/items",
        }),
        ...mapGetters({
            categories: "categories/item",
        }),
        
    },
    methods: {
        ...mapActions({
            fetchProducts: "products/fetchAll",
        }),
        ...mapActions({
            fetchCategories: "categories/fetchOne",
        }),
        prev(){
            const gsap = this.$gsap
            let whole = document.querySelectorAll('.product-card')[this.active]
            gsap.fromTo(whole, { opacity: 1,y:0 }, {y:30, opacity: 0, duration: 1 })
            this.active--
            console.log(this.active)
            if(this.active < 0){
                this.active=this.length-1
            }
        
            let whole1 = document.querySelectorAll('.product-card')[this.active]
            gsap.fromTo(whole1, { opacity: 0,y:-30 }, {y:0, opacity: 1, duration: 1,delay:0.5 })
        },
        next(){
            const gsap = this.$gsap
            let whole = document.querySelectorAll('.product-card')[this.active]
            let whole2 = document.querySelectorAll('img')[this.active]
            gsap.fromTo(whole, { opacity: 1,y:0 }, {y:30, opacity: 0, duration: 1 })
            gsap.fromTo(whole2, { opacity: 1,y:0 }, {y:30, opacity: 0, duration: 1 })
            this.active++
            console.log(this.active)
            if(this.active >= this.length){
                this.active=0
            }
        
            let whole1 = document.querySelectorAll('.product-card')[this.active]
            let whole3 = document.querySelectorAll('img')[this.active]
            gsap.fromTo(whole1, { opacity: 0,y:-30 }, {y:0, opacity: 1, duration: 1,delay:0.5 })
            gsap.fromTo(whole3, { opacity: 0,y:-30 }, {y:0, opacity: 1, duration: 1,delay:0.5 })
        }
    },
}
</script>

<style scoped>
* {
    box-sizing: border-box;
}

p {
    margin: 0;
}

body {
    /* background-color: #161516; */
    margin: 0;
}

#loader {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 100;
}

#loader .grey,
#loader .white {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

#loader .grey {
    z-index: 2;
    background-color: #1b191b;
}

#loader .white {
    z-index: 1;
    background-color: white;
}

#loader .text-wrap {
    overflow: hidden;
}

#loader .text-wrap {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    color: white;
    font-size: 70px;
    z-index: 3;
}

#loader .text-wrap span {
    display: inline-block;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 1500px;
    height: 70px;
    padding: 0 25px;
    margin: 0 auto 15px;
    position: relative;
}

header .menu {
    position: relative;
    padding-left: 1.25em;
    height: 18px;
}

header .menu:before {
    content: "";
    position: absolute;
    top: 0.25em;
    left: 0;
    width: 1.5em;
    height: 0.125em;
    border-top: 0.375em double #c9c8c9;
    border-bottom: 0.125em solid #c9c8c9;
}

header .logo {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    font-size: 30px;
    color: white;
}

header .basket {

    font-size: 13px;
    color: white;
    text-transform: uppercase;
}

header .basket span {
    color: #7b7a7b;
    margin-left: 3px;
}

#canvas-holder {
    position: relative;
    width: 100%;
    padding-top: 100%;
    margin: 0 auto;
    overflow: hidden;
}

@media screen and (min-width: 800px) {
    #canvas-holder {
        width: 50%;
        padding-top: 50%;
    }
}

@media screen and (min-width: 1100px) {
    #canvas-holder {
        width: 60%;
        padding-top: 60%;
        margin-right: 50px;
    }
}

#canvas-holder:hover .expand {
    transform: scale(1.1);
}

#canvas-holder:hover .expand>span {
    transform: scale(0.9);
}

#slider-canvas {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 2;
    cursor: pointer !important;
}

.expand {
    display: block;
    width: 50px;
    height: 50px;
    position: absolute;
    bottom: 15px;
    right: 15px;
    background-color: white;
    border-radius: 100%;
    box-shadow: 0 0 24px rgba(0, 0, 0, 0.4);
    padding: 0;
    z-index: 3;
    appearance: none;
    -webkit-appearance: none;
    border: 0;
    outline: none;
    pointer-events: none;
    cursor: pointer;
    transition: transform 0.2s ease-in-out;
}

.expand>span {
    display: block;
    width: 20px;
    height: 20px;
    margin: 0 auto;
    position: relative;
    overflow: hidden;
    transition: transform 0.2s ease-in-out;
}

.expand>span>span {
    display: block;
    width: 20px;
    height: 20px;
}

.expand>span .square {
    transform: translateY(-100%);
    border: solid 2px #333;
    opacity: 0;
}

.expand .layer {
    width: 100%;
    position: absolute;
    left: 0;
    height: 9px;
}

.expand .layer>span {
    position: absolute;
    display: block;
    width: 9px;
    height: 100%;
    box-sizing: border-box;
    border: solid 2px #333;
}

.expand .layer>span:first-child {
    left: 0;
}

.expand .layer>span:nth-child(2) {
    right: 0;
}

.expand .layer.layer--primary {
    top: 0;
}

.expand .layer.layer--secondary {
    bottom: 0;
}

.thumbs {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: stretch;
    flex-wrap: wrap;
}

.thumbs>div {
    position: absolute;
    width: 47%;
    height: 0;
    overflow: hidden;
}

.thumbs>div:nth-child(1) {
    top: 0;
    left: 0;
}

.thumbs>div:nth-child(2) {
    top: 0;
    right: 0;
}

.thumbs>div:nth-child(3) {
    top: 53%;
    left: 0;
}

.thumbs>div:nth-child(4) {
    top: 53%;
    right: 0;
}

.thumbs>div img {
    display: block;
    width: 100%;
    transform: scale(1.4);
}

#slider {
    display: flex;
    flex-direction: column;
    padding: 0 30px;
    position: relative;
    max-width: 1500px;
    margin: 0 auto 40px;
}

@media screen and (min-width: 1100px) {
    #slider {
        flex-direction: row;
        padding: 0 70px 0 40px;
    }
}

#slider article {
    position: relative;
    width: 100%;
    color: #fff;
    z-index: 2;
    max-width: 500px;
    margin: 0 auto;
}

@media screen and (min-width: 1100px) {
    #slider article {
        width: calc(40% - 50px);
        max-width: none;
    }
}

#slider article .slide-count {
    margin-top: 70px;

    font-size: 14px;
    overflow: hidden;
}

#slider article .slide-count .index {
    display: inline-block;
    position: relative;
    line-height: 24px;
    width: 16px;
    height: 24px;
}

#slider article .slide-count .index>span {
    display: block;
    height: 100%;
}

#slider article .slide-count .index .next {
    position: absolute;
    top: -100%;
    left: 0;
}

#slider article .slide-count .line {
    display: inline-block;
    width: 30px;
    height: 1px;
    background-color: white;
    vertical-align: middle;
    margin: 0 7px;
}

#slider article .slide-title {

    font-size: 70px;
    font-weight: 400;
    margin: 30px 0 30px 125px;
    letter-spacing: -3px;
    padding-left: 12px;
    line-height: 80px;
    position: relative;
}

@media screen and (min-width: 700px) {
    #slider article .slide-title {
        font-size: 110px;
        line-height: 120px;
        margin: 60px 0 60px 220px;
    }
}

@media screen and (min-width: 1100px) {
    #slider article .slide-title {
        font-size: 110px;
        line-height: 120px;
        margin-left: 50px;
    }
}

#slider article .slide-title .code {
    display: block;
    position: absolute;
    right: 100%;
    height: 100%;
    padding: 0 6px;
    overflow: hidden;
}

#slider article .slide-title .code:before {
    content: "";
    display: block;
    position: absolute;
    bottom: 0;
    left: -10px;
    width: 108%;
    height: 40%;
    background-color: #343234;
    z-index: -1;
}

#slider article .slide-title .code>span {
    position: absolute;
    top: 0;
    right: 6px;
    display: inline-block;
    height: 100%;
}

#slider article .slide-title .code .next {
    position: absolute;
    top: -100%;
}

#slider article .description {
    position: relative;
    font-size: 12px;
    line-height: 20px;
    width: 100%;
    max-width: 380px;
    height: 160px;

}

@media screen and (min-width: 1100px) {
    #slider article .description {
        height: 100px;
    }
}

#slider article .description>p {
    position: absolute;
    top: 0;
    left: 0;
}

#slider article .btn {
    margin-top: 50px;
    display: inline-block;
    position: relative;

    font-size: 13px;
    color: white;
    text-transform: uppercase;
    text-decoration: none;
}

#slider article .btn:after {
    content: "";
    display: block;
    width: 100%;
    height: 1px;
    position: absolute;
    bottom: -8px;
    background-color: #434143;
}

#slider .slide-nav {
    position: absolute;
    z-index: 5;
    top: 20px;
    right: 30px;
    transform: rotate(-90deg);
}

@media screen and (min-width: 1100px) {
    #slider .slide-nav {
        top: 50%;
        right: -50px;
        transform: translateY(-50%);
    }
}

#slider .slide-nav button {
    display: block;
    position: relative;
    appearance: none;
    -webkit-appearance: none;
    width: 40px;
    height: 40px;
    border-radius: 100%;
    border: 1px solid #434143;
    padding: 0;
    background-color: transparent;
    outline: 0;
    transition: border-color 0.3s ease-in-out;
}

#slider .slide-nav button:disabled {
    opacity: 0.2;
}

#slider .slide-nav button:hover:not(:disabled) {
    border-color: #9e969e;
    cursor: pointer;
}

#slider .slide-nav button:first-child {
    margin-bottom: 10px;
}

#slider .slide-nav button svg {
    position: absolute;
    top: 50%;
    left: 50%;
    display: block;
    width: 16px;
    height: 7px;
    fill: #9e969e;
}

#slider .slide-nav button[data-direction="prev"] svg {
    transform: translate(-50%, -50%) rotate(-90deg);
}

#slider .slide-nav button[data-direction="next"] svg {
    transform: translate(-50%, -50%) rotate(90deg);
}

#slider .dots {
    position: absolute;
    bottom: 25px;
    left: 0;
}

#slider .dots>span {
    display: inline-block;
    width: 6px;
    height: 6px;
    border-radius: 100%;
    background-color: #313131;
    margin: 0 7px 0 0;
    overflow: hidden;
}

#slider .dots>span:before {
    content: "";
    display: block;
    width: 100%;
    height: 100%;
    background-color: white;
    opacity: 0;
    transition: 0.8s opacity ease-in-out;
}

#slider .dots>span.active:before {
    opacity: 1;
}

#slider .category {
    position: absolute;
    bottom: 45px;
    right: -5px;

    font-size: 16px;
    text-transform: uppercase;
    color: white;
    transform: rotate(-90deg);
}

#slider {
    margin-bottom: 0;
}

/* Element | http://localhost:3000/cart */

.app>header:nth-child(1) {
    margin-bottom: 0px;
}

/* Element | http://localhost:3000/cart */

.app {
    height: 100%;
    /* background-color: #161516; */
    font-family: "agavalanchec";
}

.product-card {
    opacity: 0;
}

/* Element | http://localhost:7781/cart */

.expand {
    display: none;
}
#slider article .btn {
    margin-top: 30px;
    
}
</style>