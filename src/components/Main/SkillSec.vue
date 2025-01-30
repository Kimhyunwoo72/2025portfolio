<template>
    <section class="sec skill">
        <div class="skill__img" :class="{show : imgWrap}" ref="skillImg">
            <div class="img img1" :class="{ active: imgHover === 'item1' }">
                <img src="@/assets/img/HTML5-logo.png" alt="">
            </div>
            <div class="img img2" :class="{ active: imgHover === 'item2' }">
                <img src="@/assets/img/CSS3-logo.png" alt="">
            </div>
            <div class="img img3" :class="{ active: imgHover === 'item3' }">
                <img src="@/assets/img/javascript-logo.png" alt="">
            </div>
            <div class="img img4" :class="{ active: imgHover === 'item4' }">
                <img src="@/assets/img/gsap-logo.png" alt="">
            </div>
            <div class="img img5" :class="{ active: imgHover === 'item5' }">
                <img src="@/assets/img/vue-logo.png" alt="">
            </div>
            <div class="img img6" :class="{ active: imgHover === 'item6' }">
                <img src="@/assets/img/React-logo.png" alt="">
            </div>
            <div class="img img7" :class="{ active: imgHover === 'item7' }">
                <img src="@/assets/img/W3C-logo.png" alt="">
            </div>
            <div class="img img8" :class="{ active: imgHover === 'item8' }">
                <img src="@/assets/img/responsive-img.png" alt="">
            </div>
        </div>

        <div class="main-title">
            <div class="inner">
                <h2 class="tit t-r">
                    <span>FRONTEND</span>
                    <span>My skill</span>
                </h2>
            </div>
        </div>

        <div class="inner">
            <ul class="skill__list" @mouseover="imgWrap = true" @mouseout="imgWrap = false">
                <li class="skill__item skill__item1" @mouseover="imgHover = 'item1'">
                    <div class="skill__txt">
                        <div class="num">01</div>
                        <h3 class="tit">HTML5</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item2" @mouseover="imgHover = 'item2'">
                    <div class="skill__txt">
                        <div class="num">02</div>
                        <h3 class="tit">CSS3</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item3'">
                    <div class="skill__txt">
                        <div class="num">03</div>
                        <h3 class="tit">JavaScript</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item4'">
                    <div class="skill__txt">
                        <div class="num">04</div>
                        <h3 class="tit">GSAP</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item5'">
                    <div class="skill__txt">
                        <div class="num">05</div>
                        <h3 class="tit">Vue</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item6'">
                    <div class="skill__txt">
                        <div class="num">06</div>
                        <h3 class="tit">React</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item7'">
                    <div class="skill__txt">
                        <div class="num">07</div>
                        <h3 class="tit">Web Accessibility</h3>
                    </div>
                    <div class="line"></div>
                </li>
                <li class="skill__item skill__item3" @mouseover="imgHover = 'item8'">
                    <div class="skill__txt">
                        <div class="num">08</div>
                        <h3 class="tit">Responsive Web</h3>
                    </div>
                    <div class="line"></div>
                </li>
            </ul>
        </div>
    </section>


</template>

<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger);
    export default {
        data() {
            return {
                imgWrap: false,
                imgHover: ''
            }
        },
        mounted() {
            this.skillGsap()
            // 마우스 이동 이벤트
            window.addEventListener("mousemove", this.handleMouseMove);

        },
        beforeUnmount() {
            window.removeEventListener("mousemove", this.handleMouseMove);
        },
        methods: {
            skillGsap() {
                // title
                gsap.from(".skill .main-title .tit span:first-child", { scrollTrigger: { trigger: ".skill", start: "top 60%", }, ease: "power4.out", duration: 3, opacity: 0, x: 200 });
                gsap.from(".skill .main-title .tit span:last-child", { scrollTrigger: { trigger: ".skill", start: "top 60%", }, ease: "power4.out", duration: 4, delay: .2, opacity: 0, x: 200 });

                let tl = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".skill .skill__list",
                        start: "top 60%",
                        toggleClass: { targets: ".skill__item", className: 'active' },
                    }
                });

                // 첫 번째 애니메이션
                tl.from(".skill .skill__item", { ease: "power4.out", duration: 3, opacity: 0, x: 300, stagger: 0.3 }, 0)
                    .to(".skill .skill__list", { pointerEvents: 'inherit' }, 1)
                    .from(".skill .skill__item .line", { ease: "power4.out", duration: 2, opacity: 0, scale: 0, }, 0)
                    .to(".skill .skill__item .line", { duration: 2, opacity: 0.3, });
            },
            handleMouseMove(event) {
                const skillImg = this.$refs.skillImg;
                if (skillImg) {
                    const mouseX = event.clientX + window.scrollX;
                    const mouseY = event.clientY + window.scrollY;

                    skillImg.style.transform = `translate(${mouseX + 30}px, ${mouseY + -50}px)`;
                }
            },

        },

    };
</script>