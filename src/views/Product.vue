<template>
<div class="product">
    <HeaderShayna></HeaderShayna>
    <Breadcrumb :breadcrumbs="breadcrumbs"></Breadcrumb>

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="gambar_default" alt />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :nav="false" :dots="false">
                                    <div v-for="thumb in thumbs" :key="thumb" class="mr-2 pt" :class="thumb==gambar_default?'active':''">
                                        <img :src="thumb" @click="changeImage(thumb)" alt />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6 text-left">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                                        Corporis, error officia. Rem aperiam laborum voluptatum
                                        vel, pariatur modi hic provident eum iure natus quos non a
                                        sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                                        Quam possimus quisquam animi, commodi, nihil voluptate
                                        nostrum neque architecto illo officiis doloremque et
                                        corrupti cupiditate voluptatibus error illum. Commodi
                                        expedita animi nulla aspernatur. Id asperiores blanditiis,
                                        omnis repudiandae iste inventore cum, quam sint molestiae
                                        accusamus voluptates ex tempora illum sit perspiciatis.
                                        Nostrum dolor tenetur amet, illo natus magni veniam quia
                                        sit nihil dolores. Commodi ratione distinctio harum
                                        voluptatum velit facilis voluptas animi non laudantium, id
                                        dolorem atque perferendis enim ducimus? A exercitationem
                                        recusandae aliquam quod. Itaque inventore obcaecati, unde
                                        quam impedit praesentium veritatis quis beatae ea atque
                                        perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->
    <RelatedShayna></RelatedShayna>
    <FooterShayna></FooterShayna>
</div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import HeaderShayna from "@/components/HeaderShayna.vue";
import Breadcrumb from "@/components/Breadcrumb.vue";
import RelatedShayna from "@/components/RelatedShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";
import carousel from "vue-owl-carousel";

export default {
    name: "Product",
    components: {
        HeaderShayna,
        FooterShayna,
        Breadcrumb,
        RelatedShayna,
        carousel,
        // HelloWorld,
    },
    data() {
        return {
            gambar_default: "img/mickey1.jpg",
            breadcrumbs: [{
                url: "product",
                title: "Product",
            }, ],
            thumbs: [
                "img/mickey1.jpg",
                "img/mickey2.jpg",
                "img/mickey3.jpg",
                "img/mickey4.jpg",
            ],
        };
    },
    methods: {
        changeImage(urlImage) {
            this.gambar_default = urlImage;
        },
    },
};
</script>
