<script>
export default {
    data() {
        return {
            menuItems: [
                {
                    title: "Characters",
                    url: "#",
                },
                {
                    title: "Comics",
                    url: "#",
                },
                {
                    title: "Movies",
                    url: "#",
                },
                {
                    title: "TV",
                    url: "#",
                },
                {
                    title: "Games",
                    url: "#",
                },
                {
                    title: "Collectibles",
                    url: "#",
                },
                {
                    title: "Videos",
                    url: "#",
                },
                {
                    title: "Fans",
                    url: "#",
                },
                {
                    title: "News",
                    url: "#",
                },
                {
                    title: "Shop",
                    url: "#",
                },
            ]
        }
    }
}

</script>

<template>
    <header class="d-flex align-items-center justify-content-center">
        <div class="container d-flex justify-content-between align-items-center h-100">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC Logo">
            </div>
            <ul class="items d-flex m-0 p-0 h-100">
                <li v-for="(item) in menuItems"
                    class="d-flex align-items-center mx-3 h-100 ">
                    <a class="text-dark" :href="item.url">{{ item.title.toUpperCase() }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>



<style>


</style>