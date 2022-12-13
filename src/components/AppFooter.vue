<script>
export default {
    props: {
        // set props 
        links: Array,
    },
    data() {
        return {
        }
    },

}
</script>

<template>

    <!-- blue option bar -->
    <div class="top">
        <div class="container">
            <a href="">
                <img src="../assets/buy-comics-subscriptions.png" alt="">
                <h5>DIGITAL COMICS</h5>
            </a>
            <a href="">
                <img src="../assets/buy-comics-subscriptions.png" alt="">
                <h5>DIGITAL COMICS</h5>
            </a>
            <a href="">
                <img src="../assets/buy-comics-subscriptions.png" alt="">
                <h5>DIGITAL COMICS</h5>
            </a>
            <a href="">
                <img src="../assets/buy-comics-subscriptions.png" alt="">
                <h5>DIGITAL COMICS</h5>
            </a>
            <a href="">
                <img src="../assets/buy-comics-subscriptions.png" alt="">
                <h5>DIGITAL COMICS</h5>
            </a>

        </div>
    </div>

    <!-- footer -->
    <footer style="background-image: url(../src/assets/footer-bg.jpg)">
        <!-- bg dc logo (needs to fix) -->
        <img src="../assets/dc-logo-bg.png" alt="">

        <div class="container">

            <!-- footer nav -->
            <nav>

                <!-- v-for using props -->
                <div v-for="(item, index) in links" :key="index" :class="index !== 0 ? 'd-none d-lg-block' : ''">

                    <!-- nav name -->
                    <h3>{{ item.name }}</h3>

                    <!-- link list -->
                    <ul>
                        <li v-for="(item, index) in item.subitem" :key="index" :class="{ active: item.status }">
                            <a :href="item.url">{{ item.name }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </footer>

    <!-- bottom bar -->
    <div class="bottom">
        <div class="container">
            <!-- sign button -->
            <a name="" id="" class="btn btn-outline-primary rounded-0" href="#" role="button">SIGN UP NOW!</a>

            <!-- follow options -->
            <div>
                <h3>FOLLOW US</h3>
                <a href="">
                    <img src="../assets/footer-facebook.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/footer-twitter.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/footer-pinterest.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/footer-youtube.png" alt="">
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
// import scss
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
@use '../styles/general.scss' as *;


// blue bar
.top {
    background-color: $dc_blue;
    min-height: 100px;
    display: flex;
    align-items: center;

    div {
        display: flex;
        justify-content: space-between;

        a {
            color: white;

            img {
                width: 100%;
                height: auto;
                max-width: 50px;
                margin-right: 10px;
            }

            h5 {
                display: inline-block;
                font-size: 14px;
            }

            &:hover {
                filter: invert(100%)
            }
        }

    }

}

// footer
footer {
    min-height: 400px;
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;
    position: relative;
    padding: 50px 0;

    img {
        right: 0;
        top: 0;
        translate: 0% -15%;
        position: absolute;
    }

    nav {
        width: 100%;
        display: flex;
        align-items: flex-start;
        gap: 30px;

        div {
            min-width: 150px;
        }

        h3 {
            font-size: 24px;
            color: white;
            font-weight: 600;
            margin-bottom: 15px;
        }

        ul {
            margin: 0;
            padding: 0;
            list-style: none;

            li {
                a {
                    color: gray;

                    &:hover {
                        color: $dc_blue;
                    }
                }
            }
        }
    }

}

// bottom bar
.bottom {
    min-height: 80px;
    background-color: $background;
    display: flex;
    align-items: center;

    div {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 15px;
        color: $dc_blue;

        h3 {
            font-weight: 600;
            font-size: 24px;
            margin: 0;
        }

        a {
            img {
                &:hover {
                    filter: sepia(100%) hue-rotate(172deg) saturate(400%);
                }
            }
        }
    }
}
</style>