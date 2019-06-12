<template>
    <div class="about--container">
    <div class="over--container">
        <div class="about--title">
            <h2>Sobre mi</h2>
        </div>
        <div class="about--description">
            <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem vero vitae voluptatem eaque blanditiis a corrupti, quis nihil culpa vel magnam aliquid quod laudantium aut nobis est officia quisquam ullam.
            </p>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod sint tempore quidem similique, numquam eos necessitatibus nostrum voluptatem, ab officia nam perferendis labore itaque. Nihil quasi ea consectetur perferendis quia.
            </p>
        </div>
        <div class="container-knowledge">
            <a class="knowledge--link" v-on:click="showKnowledge = !showKnowledge"><span>Conocimientos</span> <font-awesome-icon :icon="['fas', 'chevron-right']" class="arrow--know" :class="{'show--know': showKnowledge}" /></a>
        </div>
    </div>
    <transition name="fade">
        <div class="knowledge--description" v-if="showKnowledge">
            <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consectetur ab iste repellendus ad, corporis amet deserunt explicabo quae eum delectus non autem, esse doloribus saepe facere expedita optio consequatur soluta.
            </p>
        </div>
    </transition>
    </div>
</template>

<script>
module.exports = {
    data: function() {
        return {
            showKnowledge: false
        }
    },
    methods: {
    }
}
</script>



<style lang="scss" scoped>
    @import '../assets/variables';
    .over--container {
        position: relative;
        z-index: 1000;
        background-color: $black;
    }
    .about--container {
        padding: 75px 90px;
        color: $principal;
        height: 100vh;
        @media only screen and(max-width: 820px) {
            padding: 25px 30px;
        }
        .about--title {
            h2 {
                letter-spacing: 3px;
            }
        }
        .about--description {
            margin-top: 60px;
            @media only screen and(max-width: 820px) {
                margin-top: 20px;
            }
            p {
                letter-spacing: 2px;
                margin-bottom: 20px;
                text-align: justify;
                @media only screen and(max-width: 390px) {
                    font-size: 14px;
                }
            }
        }
    }
    .container-knowledge {
        height: 60px;
        width: 100%;
        border-top: solid $principal 2px;
        margin-top: 60px;
        padding: 15px 0;
        @media only screen and(max-width: 820px) {
            margin-top: 25px;
        }
        .knowledge--link {
            color: $principal;
            width: 100%;
            display: block;
            position: relative;
            cursor: pointer;
        }
    }

    .knowledge--description p{
        letter-spacing: 2px;
        @media only screen and(max-width: 390px) {
            font-size: 14px;
        }
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s;
    }

    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
        opacity: 0;
    }

    .arrow--know {
        transition: all .9s;
        position: absolute;
        transform: none;
        margin-left: 10px;
        &.show--know {
            transition: all ease-in .9s;
            right: 0;
            transform: rotate(90deg);
        }
    }


</style>
