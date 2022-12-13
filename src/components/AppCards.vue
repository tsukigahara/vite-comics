<script>
export default {
    props: {
        // set props
        links: Array
    }
}
</script>

<template>
    <section>
        <!-- jumbo div -->
        <div class="jumbo" style="background-image: url(../src/assets/jumbotron.jpg)">
            <!-- title -->
            <div class="section_title">
                CURRENT SERIES
            </div>
        </div>
        <!-- contents -->
        <div class="container p-5">
            <!-- bootrap grid system -->
            <div class="row row-cols-lg-6 row-cols-md-4 row-cols-sm-3 row-cols-2 g-3">
                <!-- vfor using props -->
                <div class="col" v-for="(item, index) in links" :key="index">
                    <!-- card -->
                    <div class="card bg-transparent">
                        <!-- vard image -->
                        <img :src="item.thumb" class="card-img-top rounded-0" :alt="item.series">
                        <!-- card boby -->
                        <div class="card-body px-0">
                            <!-- card title -->
                            <h5 class="card-title">{{ item.series }}</h5>
                            <!-- <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                                additional
                                content. This content is a little bit longer.</p> -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
// import scss
@use '../styles/partials/variables' as *;

h5 {
    font-size: 16px;
    font-weight: 600;
    color: white;
}

section {
    background-color: black;

    .jumbo {
        min-height: 300px;
        position: relative;
        background-size: cover;
        background-position: 50% 0%;

        .section_title {
            padding: 10px 20px;
            background-color: $dc_blue;
            color: white;
            font-size: 18px;
            font-weight: 600;
            position: absolute;
            bottom: 0;
            left: 5%;
            translate: 0% 50%;

        }
    }

}
</style>