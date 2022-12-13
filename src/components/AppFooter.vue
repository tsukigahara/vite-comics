<script>
export default {
    props: {
        links: Array,
    },
    data() {
        return {
        }
    },

}
</script>

<template>
    <footer style="background-image: url(../src/assets/footer-bg.jpg)">
        <img src="../assets/dc-logo-bg.png" alt="">
        <div class="container">
            <nav>
                <div v-for="(item, index) in links" :key="index">
                    <h3>{{ item.name }}</h3>
                    <ul>
                        <li v-for="(item, index) in item.subitem" :key="index" :class="{ active: item.status }">
                            <a :href="item.url">{{ item.name }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer {
    min-height: 400px;
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;
    position: relative;

    img {
        right: 0;
        top: 0;
        translate: 0% -15%;
        position: absolute;
    }

    nav {
        display: flex;
        width: 100%;
    }
}
</style>