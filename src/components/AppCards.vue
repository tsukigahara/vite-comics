<script>
export default {
    props: {
        links: Array
    }
}
</script>

<template>
    <section>
        <div class="jumbo">
            <img src="../assets/" alt="">
        </div>
        <div class="container p-5">
            <div class="row row-cols-lg-6 row-cols-md-4 row-cols-sm-3 row-cols-2 g-3">
                <div class="col" v-for="(item, index) in links" :key="index">
                    <div class="card bg-transparent">
                        <img :src="item.thumb" class="card-img-top" :alt="item.series">
                        <div class="card-body pt-3">
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
h5 {
    font-size: 16px;
    font-weight: 600;
    color: white;
}

section {
    background-color: black;
}
</style>