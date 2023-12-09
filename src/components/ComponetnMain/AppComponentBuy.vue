<script>
export default {
    name: "Buy",
    data() {
        return {
            buyContents: [
                {
                    title: "Digital Comics",
                    path: "../../assets/img/buy-comics-digital-comics.png"
                },
                {
                    title: "DC Merchandise",
                    path: "../../assets/img/buy-comics-merchandise.png"
                },
                {
                    title: "Subscription",
                    path: "../../assets/img/buy-comics-subscriptions.png"
                },
                {
                    title: "Comic Shop Locator",
                    path: "../../assets/img/buy-comics-shop-locator.png"
                },
                {
                    title: "DC Power",
                    path: "../../assets/img/buy-dc-power-visa.svg"
                },
            ]
        }
    }
}
</script>
<template>
    <div class="buy">
        <ul>
            <li v-for='content in buyContents'>
                <div class="image">
                    <img src="../../assets/img/buy-dc-power-visa.svg" alt="img">
                </div>
                <div class="content"> {{ content.title }}
                </div>
            </li>
        </ul>
    </div>
</template>
<style scoped lang="scss">
@use "../../style/variable.scss" as *;

div.buy {
    background-color: $color-bar;
    @include padding-standard;

    ul {
        display: flex;
        justify-content: space-between;
        padding: 40px 0;
        color: white;
        gap: 10px;

        li {
            display: flex;
            align-items: center;
            gap: 10px;

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