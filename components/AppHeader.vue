// Used nuxt-links in compenent to use in default.vue layout thorughout the project //
<template>
    <header class="header">
        <img class="header-img" src="~/assets/garden-logo.svg" />
        <nav class="navbar navbar-light" style="background-color: #0b160b;">
            <ul class="nav justify-content-center">
                <li>
                    <nuxt-link  to='/'>Home</nuxt-link>  
                </li>
                <li>
                    <nuxt-link to='/inspired'>Get Inspired</nuxt-link>
                </li>
                <li>
                    <nuxt-link to='/common'>Common Terms</nuxt-link>
                </li>
                <li>
                    <nuxt-link to='/about'>About</nuxt-link>
                </li>
                <li>
                    <nuxt-link to='/jokes'>Jokes</nuxt-link>
                </li>
            </ul>
        </nav>
    </header>
</template>


<style>
.header-img {
    padding: 1rem 0 1rem 2rem;
    width: 12rem;
 }
.navbar {
    padding-left: 2rem;
}
.nav li a {
    color: #fff;
    padding-right: 2rem;
}
.nav li a:hover {
    color: #b8b6b6;
}
</style>
