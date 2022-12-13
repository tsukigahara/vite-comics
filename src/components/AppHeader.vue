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

    <header>
        <div class="container">
            <div>
                <a href="">
                    <img src="../assets/dc-logo.png" alt="">
                </a>
                <nav class="d-none d-lg-block">
                    <ul>
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
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

header {
    background-color: white;
    font-size: $headerfont;
    font-weight: 600;

    .container {
        div {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            min-height: 100px;
        }
    }
}


a>img {
    width: 80px;
    height: auto;
}

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