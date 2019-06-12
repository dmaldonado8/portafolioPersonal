<template>
    <div class="proyecto--container" :style="{ backgroundImage: `url(${image})` }" @mouseover.stop="showDescription = true" @mouseout.stop="showDescription = false">
        <div class="proyecto--descripcion" v-show="showDescription">
            <div class="proyecto--title">
                <h3>{{ title }}</h3>
            </div>
            <div class="proyecto--text--description">
                <p>{{ description }}</p>
            </div>
        </div>
    </div>
</template>

<script>
module.exports = {
    data: function() {
        return {
            showDescription: false
        }
    },
    props: {
        image: String,
        title: String,
        description: String
    }
}
</script>


<style lang="scss" scoped>
    @import '../assets/variables';
    .proyecto--container {
        width: 100%;
        height: 350px;
        background: red;
        background-size: cover;
        position: relative;
        img {
            max-height: 100%;
            max-width: 100%;
        }
        .proyecto--descripcion {
            height: 100%;
            width: 100%;
            background-color: rgba(0, 0, 0, .5);
            position: absolute;
            z-index: 1000;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            & > * {
                color: $principal;
            }
            .proyecto--title {
                padding: 20px;
            }
            .proyecto--text--description {
                padding: 20px;
            }
        }
    }
</style>