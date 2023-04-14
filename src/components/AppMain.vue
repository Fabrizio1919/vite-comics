<script>
import dcComics from "../assets/data/dc-comics.json"
import ItemsComicx from "./ItemsComicx.vue";
export default {
    name:'AppMain',
    components: {
        ItemsComicx
    },
    data() {
        return {
            dcComics: dcComics,
            ShopSites: [
                {
                    img: "../src/assets/img/buy-comics-digital-comics.png",
                    title: "Digital comics",
                    link: "#",
                },
                {
                    img: "../src/assets/img/buy-comics-merchandise.png",
                    title: "DC merchandise",
                    link: "#",
                },
                {
                    img: "../src/assets/img/buy-comics-subscriptions.png",
                    title: "Subscription",
                    link: "#",
                },
                {
                    img: "../src/assets/img/buy-comics-shop-locator.png",
                    title: "Comic shop locator",
                    link: "#",
                },
                {
                    img: "../src/assets/img/buy-dc-power-visa.svg",
                    title: "DC power visa",
                    link: "#",
                },
            ]
        }
    },
}

</script>

<template>
    <main>
        <div id="jumbo"></div>
        <section id="main_content" class="bg-dark">
            <div class="container">
                <div class="m-0 py-5 text-light">
                    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4 row-cols-lg-6">
                        
                            <ItemsComicx :thumb="product.thumb" :series="product.series"  :price="product.price" v-for="product in dcComics"/>
                        
                    </div>
                </div>
            </div>
        </section>
        <section id="sites_shop">
            <ul class="container d-flex justify-content-between align-items-center py-5 text-light">
                <li v-for="site in ShopSites" class="mx-4">
                    <img height="50" :src="site.img" :alt="site.title.toUpperCase() + ' Image'" class="me-2">
                    <a :href="site.link" class="text-light">{{ site.title.toUpperCase() }}</a>
                </li>
            </ul>
        </section>
    </main>
</template>

<style>


/* #sites_shop {
  background-color: #0282f9;
}
li {
    list-style: none;
}
a {
    text-decoration:none;
}
 */


</style>