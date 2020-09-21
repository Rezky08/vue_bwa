<template>
<!-- Related Products Section End -->
<div class="related-products spad">
    <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <div class="section-title">
                    <h2>Related Products</h2>
                </div>
            </div>
        </div>
        <div class="row">
            <div v-for="(product, index) in products" :key="index" class="col-lg-3 col-sm-6">
                <div class="product-item">
                    <div class="pi-pic">
                        <img :src="product.image" alt />
                        <ul>
                            <li class="w-icon active">
                                <a href="#">
                                    <i class="icon_bag_alt"></i>
                                </a>
                            </li>
                            <li class="quick-view">
                                <a href="#">+ Quick View</a>
                            </li>
                        </ul>
                    </div>
                    <div class="pi-text">
                        <div class="catagory-name">{{product.category}}</div>
                        <a href="#">
                            <h5>{{product.name}}</h5>
                        </a>
                        <div class="product-price">
                            {{product.price_disc?product.price_disc:product.price}}
                            <span v-show="product.price_disc">{{product.price}}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
<!-- Related Products Section End -->
</template>

<script>
export default {
    name: "RelatedShayna",
    data() {
        return {
            products: [{
                    image: "img/products/women-1.jpg",
                    name: "Pure Pineapple",
                    category: "Coat",
                    price: "$35.00",
                    price_disc: "$14.00",
                },
                {
                    image: "img/products/women-2.jpg",
                    name: "Guangzhou Sweater",
                    category: "Shoes",
                    price: "$13.00",
                },
                {
                    image: "img/products/women-3.jpg",
                    name: "Pure Pineapple",
                    category: "Towel",
                    price: "$34.00",
                },
                {
                    image: "img/products/women-4.jpg",
                    name: "Converse Shoes",
                    category: "Towel",
                    price: "$34.00",
                },
            ],
        };
    },
};
</script>
