<template>
    <div class="navbar--main--page">
        <nav class="navbar">
            <div class="logo--nav">
                <h1>DMC</h1>
            </div>
            <div class="nav--links">
                <ul>
                    <li><nuxt-link to="/">Inicio</nuxt-link></li>
                    <li><nuxt-link to="/portfolio">Proyectos</nuxt-link></li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<style lang="scss">
    @import '../assets/variables';
    
    .navbar--main--page {
        height: 9vh;
        background-color: $principal;
        width: 100%;
        padding: 30px;
    }
    nav.navbar {
        display: flex;
        justify-content: space-between;
        height: 100%;
        .logo--nav {
            display: inherit;
            align-items: center;
        }
        .nav--links {
            display: inherit;
            align-items: center;
            height: 100%;
            ul {
                display: flex;
                &:nth-child(1) li {
                    margin-right: 15px;
                }
                li > a {
                    transition: all .3s;
                    padding: 5px 10px;
                    border-radius: 20px;
                    font-size: 15px;
                    &:hover {
                        color: $principal;
                        background-color: black;
                    }
                }
            }
        }
    }
</style>
