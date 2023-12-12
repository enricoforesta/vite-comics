<script>
export default {
    name: "Buy",
    data() {
        return {
            buyContents: [
                {
                    title: "Digital Comics",
                    path: "../../assets/img/buy-comics-digital-comics.png",
                },
                {
                    title: "DC Merchandise",
                    path: "../../assets/img/buy-comics-merchandise.png",
                },
                {
                    title: "Subscription",
                    path: "../../assets/img/buy-comics-subscriptions.png",
                },
                {
                    title: "Comic Shop Locator",
                    path: "../../assets/img/buy-comics-shop-locator.png",
                },
                {
                    title: "DC Power",
                    path: "../../assets/img/buy-dc-power-visa.svg",
                },
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        },
    }
}
</script>
<template>
    <div class="buy">
        <ul>
            <li v-for='content in buyContents'>
                <div class="image">
                    <!-- <img src="../../assets/img/buy-comics-digital-comics.png" alt=""> -->
                    <img :src="getImagePath(content.path)" :alt="content.title">
                </div>
                <div class="content">
                    <a href="#">{{ content.title.toUpperCase() }}</a>
                </div>
            </li>
        </ul>
    </div>
</template>
<style scoped lang="scss">
@use "../../style/partials/variable.scss" as *;
@use "../../style/partials/mixin.scss" as *;

div.buy {
    background-color: $color-bar;
    @include padding-standard;

    ul {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding: 60px 0;
        color: $color-text-white;
        gap: 10px;

        li {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 20px;

            div.image {
                width: 45px;
                display: flex;

                img {
                    width: 100%;
                }
            }
        }
    }
}
</style>