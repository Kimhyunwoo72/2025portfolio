<template>
    <section class="sec suspicious">
        <div class="suspicious__top">
            <div class="line"></div>
            <div class="main-title">
                <div class="inner">
                    <h2 class="tit">
                        <span>FRONTEND</span>
                        <span>Suspicious</span>
                    </h2>
                    <div class="desc">
                        참여한 프로젝트 중 웹어워드를 수상한 작품을 소개합니다.
                        저의 전문성과 열정을 담아낸 결과물입니다.
                    </div>
                </div>
            </div>
        </div>
        <ul class="suspicious__list">
            <li class="suspicious__item suspicious__item1">
                <div class="line"></div>
                <div class="top">
                    <div class="inner">
                        <span>FRONTEND DEVELOPER 2023</span>
                        <span>PROJECT</span>
                    </div>
                </div>
                <div class="line"></div>
                <div class="cont">
                    <div class="suspicious__img">
                        <div class="img">
                            <img src="@/assets/img/suspicious-img1.jpg" alt="">
                            <div class="bg"></div>
                        </div>
                        <div class="line2"></div>
                    </div>
                    <div class="suspicious__text">
                        <div class="suspicious__detail">
                            <h3 class="title">고려대학교 의료원 리뉴얼</h3>
                            <p class="desc">
                                2023년 웹 어워드 모바일 이노베이션대상
                            </p>
                        </div>
                        <div class="more">
                            <a href="https://www.kumc.or.kr/kr/index.do" target="_blank" title="새칭열림">VIEW SITE</a>
                        </div>
                    </div>
                </div>
                <div class="line"></div>
            </li>
            <li class="suspicious__item suspicious__item2">
                <div class="line"></div>
                <div class="top">
                    <div class="inner">
                        <span>FRONTEND DEVELOPER 2023</span>
                        <span>PROJECT</span>
                    </div>
                </div>
                <div class="line"></div>
                <div class="cont">
                    <div class="suspicious__img">
                        <div class="img">
                            <img src="@/assets/img/suspicious-img2.jpg" alt="">
                            <div class="bg"></div>
                        </div>
                        <div class="line2"></div>
                    </div>
                    <div class="suspicious__text">
                        <div class="suspicious__detail">
                            <h3 class="title">고려대학교 의과대학 리뉴얼</h3>
                            <p class="desc">
                                2023년 웹어워드 교육부분 통합 대상
                            </p>
                        </div>
                        <div class="more">
                            <a href="https://medicine.korea.ac.kr/kr/index.do" target="_blank" title="새칭열림">VIEW SITE</a>
                        </div>
                    </div>
                </div>
                <div class="line"></div>
            </li>
            <li class="suspicious__item suspicious__item3">
                <div class="line"></div>
                <div class="top">
                    <div class="inner">
                        <span>FRONTEND DEVELOPER 2023</span>
                        <span>PROJECT</span>
                    </div>
                </div>
                <div class="line"></div>
                <div class="cont">
                    <div class="suspicious__img">
                        <div class="img">
                            <img src="@/assets/img/suspicious-img3.jpg" alt="">
                            <div class="bg"></div>
                        </div>
                        <div class="line2"></div>
                    </div>
                    <div class="suspicious__text">
                        <div class="suspicious__detail">
                            <h3 class="title">고려대학교 안암병원 리뉴얼</h3>
                            <p class="desc">
                                2023년 웹어워드 의료부분 통합대상
                            </p>
                        </div>
                        <div class="more">
                            <a href="https://anam.kumc.or.kr/kr/index.do" target="_blank" title="새칭열림">VIEW SITE</a>
                        </div>
                    </div>
                </div>
                <div class="line"></div>
            </li>
            <li class="suspicious__item suspicious__item4">
                <div class="line"></div>
                <div class="top">
                    <div class="inner">
                        <span>FRONTEND DEVELOPER 2023</span>
                        <span>PROJECT</span>
                    </div>
                </div>
                <div class="line"></div>
                <div class="cont">
                    <div class="suspicious__img">
                        <div class="img">
                            <img src="@/assets/img/suspicious-img4.jpg" alt="">
                            <div class="bg"></div>
                        </div>
                        <div class="line2"></div>
                    </div>
                    <div class="suspicious__text">
                        <div class="suspicious__detail">
                            <h3 class="title">우리금융저축은행</h3>
                            <p class="desc">
                                통합 포탈 구축 2023년 웹어워드 은행분야 대상 수상
                            </p>
                        </div>
                        <div class="more">
                            <a href="https://www.woorisavingsbank.com/" target="_blank" title="새칭열림">VIEW SITE</a>
                        </div>
                    </div>
                </div>
                <div class="line"></div>
            </li>
            <li class="suspicious__item suspicious__item5">
                <div class="line"></div>
                <div class="top">
                    <div class="inner">
                        <span>FRONTEND DEVELOPER 2024</span>
                        <span>PROJECT</span>
                    </div>
                </div>
                <div class="line"></div>
                <div class="cont">
                    <div class="suspicious__img">
                        <div class="img">
                            <img src="@/assets/img/suspicious-img5.jpg" alt="">
                            <div class="bg"></div>
                        </div>
                        <div class="line2"></div>
                    </div>
                    <div class="suspicious__text">
                        <div class="suspicious__detail">
                            <h3 class="title">창원파티마병원</h3>
                            <p class="desc">
                                2024년 웹어워드 종합의료분야 최우수상
                            </p>
                        </div>
                        <div class="more">
                            <a href="https://www.fatimahosp.co.kr/" target="_blank" title="새칭열림">VIEW SITE</a>
                        </div>
                    </div>
                </div>
                <div class="line"></div>
            </li>
        </ul>

    </section>
</template>
<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger);
    export default {
        data() {
            return {
            }
        },
        methods: {
            suspiciousGsap() {

                // gsap.from(".suspicious .main-title .tit span:first-child", { scrollTrigger: { trigger: ".suspicious", start: "top center", }, ease: "power4.out", duration: 3, opacity: 0, x: 200 });
                // gsap.from(".suspicious .main-title .tit span:last-child", { scrollTrigger: { trigger: ".suspicious", start: "top center", }, ease: "power4.out", duration: 4, delay: .2, opacity: 0, x: 200 });
                // gsap.from(".suspicious .main-title .desc", { scrollTrigger: { trigger: ".suspicious", start: "top center", }, ease: "power4.out", duration: 4, delay: .2, opacity: 0, x: 200 });


                const tl = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".suspicious", // 트리거 요소
                        start: "top center", // 애니메이션 시작 지점
                    },
                });
                tl.from('.suspicious__top .line', { scale: 0, duration: 1 })
                    .from(".suspicious .main-title .tit span:first-child", { ease: "power4.out", duration: 3, opacity: 0, x: 200 }, .6)
                    .from(".suspicious .main-title .tit span:last-child", { ease: "power4.out", duration: 4, opacity: 0, x: 200 }, .8)
                    .from(".suspicious .main-title .desc", { ease: "power4.out", duration: 5, opacity: 0, }, .9)
                    .from('.suspicious__item1 .line', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from('.suspicious__item1 .line2', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from(".suspicious__item1 .top span", { ease: "power4.out", duration: 5, opacity: 0, }, .9)
                    .from(".suspicious__item1 .img .bg", { ease: "power4.out", duration: 2, height: '100%', }, .9)
                    .from(".suspicious__item1 .suspicious__text .title", { ease: "power4.out", duration: 2, opacity: 0, x: 40 }, .9)
                    .from(".suspicious__item1 .suspicious__text .desc", { ease: "power4.out", duration: 2, opacity: 0, x: 60 }, .9)
                    .from(".suspicious__item1 .suspicious__text .more", { ease: "power4.out", duration: 2, opacity: 0 }, 1)

                const tl2 = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".suspicious__item2", // 트리거 요소
                        start: "-20% center", // 애니메이션 시작 지점
                        // markers: true,
                    },
                });
                tl2.from('.suspicious__item2 .line', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from('.suspicious__item2 .line2', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from(".suspicious__item2 .top span", { ease: "power4.out", duration: 5, opacity: 0, }, 1)
                    .from(".suspicious__item2 .img .bg", { ease: "power4.out", duration: 2, height: '100%', }, .9)
                    .from(".suspicious__item2 .suspicious__text .title", { ease: "power4.out", duration: 2, opacity: 0, x: 40 }, .9)
                    .from(".suspicious__item2 .suspicious__text .desc", { ease: "power4.out", duration: 2, opacity: 0, x: 60 }, .9)
                    .from(".suspicious__item2 .suspicious__text .more", { ease: "power4.out", duration: 2, opacity: 0 }, 1)

                const tl3 = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".suspicious__item3", // 트리거 요소
                        start: "-20% center", // 애니메이션 시작 지점

                    },
                });
                tl3.from('.suspicious__item3 .line', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from('.suspicious__item3 .line2', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from(".suspicious__item3 .top span", { ease: "power4.out", duration: 5, opacity: 0, }, 1)
                    .from(".suspicious__item3 .img .bg", { ease: "power4.out", duration: 2, height: '100%', }, .9)
                    .from(".suspicious__item3 .suspicious__text .title", { ease: "power4.out", duration: 2, opacity: 0, x: 40 }, .9)
                    .from(".suspicious__item3 .suspicious__text .desc", { ease: "power4.out", duration: 2, opacity: 0, x: 60 }, .9)
                    .from(".suspicious__item3 .suspicious__text .more", { ease: "power4.out", duration: 2, opacity: 0 }, 1)

                const tl4 = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".suspicious__item4", // 트리거 요소
                        start: "-20% center", // 애니메이션 시작 지점

                    },
                });
                tl4.from('.suspicious__item4 .line', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from('.suspicious__item4 .line2', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from(".suspicious__item4 .top span", { ease: "power4.out", duration: 5, opacity: 0, }, 1)
                    .from(".suspicious__item4 .img .bg", { ease: "power4.out", duration: 2, height: '100%', }, .9)
                    .from(".suspicious__item4 .suspicious__text .title", { ease: "power4.out", duration: 2, opacity: 0, x: 40 }, .9)
                    .from(".suspicious__item4 .suspicious__text .desc", { ease: "power4.out", duration: 2, opacity: 0, x: 60 }, .9)
                    .from(".suspicious__item4 .suspicious__text .more", { ease: "power4.out", duration: 2, opacity: 0 }, 1);

                const tl5 = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".suspicious__item5", // 트리거 요소
                        start: "-20% center", // 애니메이션 시작 지점

                    },
                });
                tl5.from('.suspicious__item5 .line', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from('.suspicious__item5 .line2', { scale: 0, duration: 1.3, stagger: 0.3 }, 0)
                    .from(".suspicious__item5 .top span", { ease: "power4.out", duration: 5, opacity: 0, }, 1)
                    .from(".suspicious__item5 .img .bg", { ease: "power4.out", duration: 2, height: '100%', }, .9)
                    .from(".suspicious__item5 .suspicious__text .title", { ease: "power4.out", duration: 2, opacity: 0, x: 40 }, .9)
                    .from(".suspicious__item5 .suspicious__text .desc", { ease: "power4.out", duration: 2, opacity: 0, x: 60 }, .9)
                    .from(".suspicious__item5 .suspicious__text .more", { ease: "power4.out", duration: 2, opacity: 0 }, 1)



                gsap.matchMedia().add("(min-width: 1025px)", () => {
                    gsap.to(".suspicious__top", {
                        scrollTrigger: {
                            trigger: ".suspicious",
                            start: "top top",
                            end: "bottom-=800px",
                            toggleClass: { targets: ".suspicious__top", className: "active" },
                        },
                    });

                    gsap.to(".suspicious__top", {
                        scrollTrigger: {
                            trigger: ".suspicious",
                            start: "bottom-=800px top",
                            end: "bottom",
                            toggleClass: { targets: ".suspicious__top", className: "stay" },
                        },
                    });
                });
                gsap.matchMedia().add("(min-width: 721px) and (max-width: 1023px)", () => {
                    gsap.to(".suspicious__top", {
                        scrollTrigger: {
                            trigger: ".suspicious",
                            start: "top top",
                            end: "bottom-=850px",
                            toggleClass: { targets: ".suspicious__top", className: "active" },
                        },
                    });

                    gsap.to(".suspicious__top", {
                        scrollTrigger: {
                            trigger: ".suspicious",
                            start: "bottom-=850px top",
                            end: "bottom",
                            toggleClass: { targets: ".suspicious__top", className: "stay" },
                        },
                    });
                });
            }
        },
        mounted() {
            this.suspiciousGsap()
        },

    };
</script>