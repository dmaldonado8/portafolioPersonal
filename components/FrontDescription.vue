<template>
    <div class="description--container">
        <div class="description">
            <div class="description--texts">
                <div class="description--title">
                    <h1><span class="text--name">David Maldonado</span> desarrollador web.</h1>
                </div>
                <hr class="title--separator">
                <div class="description--text">
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequatur, amet enim excepturi doloremque alias.</p>
                </div>
                <div class="social--links">
                    <ul>
                        <li class="social--link"><a href="https://github.com/dmaldonado8"><font-awesome-icon :icon="['fab', 'github']"/></a></li>
                        <li class="social--link"><a href="https://www.linkedin.com/in/dmaldonadocardenas"><font-awesome-icon :icon="['fab', 'linkedin-in']"/></a></li>
                        <li class="social--link"><a href="#"><font-awesome-icon :icon="['fab', 'instagram']"/></a></li>
                    </ul>
                </div>
            </div>
            <div class="description--image">
                <img src="https://images.vexels.com/media/users/3/128109/isolated/preview/19620a1b49b2bd2385c816532c57f61d-isometric-mac-computer-by-vexels.png" alt="">
            </div>
        </div>
        <span class="scroll--action--container">
            <div class="arrows">
                <span class="arrow"><font-awesome-icon :icon="['fas', 'angle-down']"/></span>
                <span class="arrow"><font-awesome-icon :icon="['fas', 'angle-down']"/></span>
                <span class="arrow"><font-awesome-icon :icon="['fas', 'angle-down']"/></span>
            </div>
        </span>
    </div>
</template>

<style lang="scss" scoped>
    @import '../assets/variables';
    @import url('https://fonts.googleapis.com/css?family=Libre+Baskerville&display=swap');
    .description--container {
        padding: 15px 30px 30px 30px;
        height: 91vh;
        /*background: linear-gradient(to bottom, rgba(250,250,250,1) 0%, rgba(250,250,250,1) 56%, rgba(166,166,166,1) 74%, rgba(133,133,133,1) 81%, rgba(40,40,40,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#fafafa', endColorstr='#282828', GradientType=0 );
        */
        background-color: $principal;
    }
    .description {
        background-color: transparent;
        height: calc(100% - 50px);
        display: flex;
        justify-content: space-around;
        align-content: center;
        align-items: center;
        .description--image {
            height: 450px;
            width: 450px;
            display: flex;
            align-items: center;
            border-radius: 50%;
            border-color: $black;
            justify-content: center;
            align-content: center;
            img {
                height: 310px;
            }
            @media only screen and(max-width: 820px) {
                display: none;
            }
        }
        .description--texts {
            margin: auto;
            padding: 20px 80px;
            .description--title {
                font-size: 20px;
                color: $black;
                font-family: 'Libre Baskerville', serif;
                z-index: 99;
                position: relative;
                &::after {
                    content: '';
                    position: absolute;
                    height: 110%;
                    width: 100%;
                    background-color: rgba(249, 249, 249, 0);
                    top: 0;
                    animation-name: difuminarAnimacion;
                    animation-duration: 4s;
                }
                h1 > .text--name {
                    color: $secundario;
                }
                h1 {
                    opacity: 50;
                }
            }
            .title--separator {
                height: 4px;
                width: 30%;
                background-color: $black;
                border-style: none;
                margin-top: 15px;
                margin-bottom: 15px;
                animation-name: divisorAnimacion;
                animation-duration: 4s;
            }
            .description--text p {
                color: $black;
                font-size: 19px;
                position: relative;
                z-index: 100;
                text-align: justify;
            }
            .social--links {
                display: flex;
                justify-content: flex-end;
                margin-top: 10px;
                ul {
                    display: inline-flex;
                }
                .social--link {
                    padding: 5px;
                    a {
                        color: $black;
                        font-size: 25px;
                    }
                }
            }
            @media only screen and(max-width: 820px) {
                padding: 20px 0;
            }
        }
    }

    .scroll--action--container {
        display: flex;
        justify-content: center;
        height: 50px;
        .arrows {
            display: flex;
            flex-direction: column;
            .arrow {
                font-size: 30px;
                height: 12px;
                color: $black;
                animation-name: arrowColor;
                animation-duration: 1s;
                animation-timing-function: linear;
                animation-iteration-count: infinite;
                animation-direction: normal;
                animation-timing-function: ease;
                animation-fill-mode: forwards;
            }
            .arrow:nth-child(1){
                animation-delay: .2s;
            }
            .arrow:nth-child(2) {
                animation-delay: .3s;
            }
            .arrow:nth-child(3){
                animation-delay: .4s;
            }
        }
    }

    @keyframes arrowColor {
        0% {
            color: white;
        }
        100% {
            color: $black;
        }
    }

    @keyframes divisorAnimacion {
        0%  {
            width: 0%
        }
        100% {
            width: 30%
        }
    }

    @keyframes difuminarAnimacion {
        0% {
            background-color:rgba(249, 249, 249, .9);
        }
        100% {
            background-color:rgba(249, 249, 249, 0);
        }
    }
</style>
