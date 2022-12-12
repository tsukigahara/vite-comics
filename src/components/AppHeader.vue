<script>
import 'bootstrap';
export default {

}
</script>

<template>

    <header>
        <a href="">
            <img src="../assets/dc-logo.png" alt="">
        </a>
        <ul>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
            <li>
                <a href="">lorem</a>
            </li>
        </ul>

    </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    min-height: 100px;
    background-color: beige;
}

a>img {
    width: 80px;
    height: auto;
}

ul {
    height: 100%;
    margin: 0 20px;
    list-style: none;
    display: flex;
    gap: 0 30px;

    li {
        height: 100%;
        display: inline-block;

        a {
            text-decoration: none;
        }

    }
}
</style>