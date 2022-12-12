<script>
import 'bootstrap';
export default {

    data() {
        return {
            navlist: [
                {
                    name: 'DC COMICS',
                    subitem: [
                        {
                            name: "CHARACTER",
                            url: '',
                        },
                        {
                            name: "COMICS",
                            url: '',
                        },
                        {
                            name: "MOVIES",
                            url: '',
                        },
                        {
                            name: "TV",
                            url: '',
                        },
                        {
                            name: "GAMES",
                            url: '',
                        },
                        {
                            name: "COLLECTIBLES",
                            url: '',
                        },
                        {
                            name: "VIDEOS",
                            url: '',
                        },
                        {
                            name: "FANS",
                            url: '',
                        },
                        {
                            name: "NEWS",
                            url: '',
                        },
                        {
                            name: "SHOP",
                            url: '',
                        },

                    ]
                },
                {
                    name: 'SHOP',
                    subitem: [
                        {
                            name: 'Shop DC',
                            url: ''
                        },
                        {
                            name: 'Shop DC Collectibles',
                            url: ''
                        },
                    ]
                },
                {
                    name: 'DC',
                    subitem: [
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                    ]
                },
                {
                    name: 'SITES',
                    subitem: [
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                        {
                            name: 'lorem',
                            url: ''
                        },
                    ]
                }
            ],
            index: 0,
        }
    },

}
</script>

<template>
    <footer style="background-image: url(../src/assets/footer-bg.jpg)">
        <img src="../assets/dc-logo-bg.png" alt="">
        <div class="container">
            <nav>
                <div>
                    <ul v-for="(item, index) in navlist" :key="index">
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

    img {
        z-index: 0;
        float: right;
    }
}
</style>