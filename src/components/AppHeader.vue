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
    <!-- header -->
    <header>
        <div class="container">

            <!-- flex wrapper -->
            <div>
                <!-- logo -->
                <a href="">
                    <img src="../assets/dc-logo.png" alt="">
                </a>
                <!-- nav -->
                <nav class="d-none d-lg-block">
                    <ul>
                        <!-- vfor using props -->
                        <li v-for="(item, index) in links[0].subitem" :key="index" :class="{ active: item.status }">
                            <a :href="item.url">{{ item.name }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>
// import scss
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

header {
    background-color: white;
    font-size: $headerfont;
    font-weight: 600;

    .container {

        // flex wrapper
        div {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            min-height: 100px;
        }
    }
}

// logo
a>img {
    width: 80px;
    height: auto;
}

// nav list
ul {
    align-self: stretch;
    margin: 0;
    padding: 0;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;

    li {
        height: 100px;
        display: flex;
        align-items: center;
        border-top: 4px solid transparent;
        border-bottom: 4px solid transparent;

        a {
            text-decoration: none;
            color: $black;
        }

        &.active,
        &:hover {
            border-bottom: 4px solid $dc_blue;

            & a {
                color: $dc_blue;
            }
        }
    }
}
</style>