<script>
export default {
    name: "MainBottom",
    data() {
        return {
            lists: [
                {
                    title: "DC Comics",
                    listContent: [
                        { text: "Characters", link: "#" },
                        { text: "TV", link: "#" },
                        { text: "Movies", link: "#" },
                        { text: "Games", link: "#" },
                        { text: "Videos", link: "#" },
                        { text: "News", link: "#" }
                    ]
                },
                {
                    title: "DC",
                    listContent: [
                        { text: "Privacy Policy", link: "#" },
                        { text: "Ad Choices", link: "#" },
                        { text: "Advertising", link: "#" },
                        { text: "Jobs", link: "#" },
                        { text: "Subscriptions", link: "#" },
                        { text: "Talent Workshops", link: "#" },
                        { text: "Ratings", link: "#" }
                    ]
                },
                {
                    title: "Sites",
                    listContent: [
                        { text: "DC Magazine", link: "#" },
                        { text: "DC Kids", link: "#" },
                        { text: "DC Universe", link: "#" },
                        { text: "DC Power Visa", link: "#" }
                    ]
                },
                {
                    title: "Shop",
                    listContent: [
                        { text: "Shop DC", link: "#" },
                        { text: "Shop Help", link: "#" }
                    ]
                }
            ]
        }
    },

}
</script>
<template>
    <div class="container">
        <div class="content">
            <div v-for="list in lists" class="list">
                <h3>{{ list.title.toUpperCase() }}</h3>
                <ul>
                    <li v-for="text in list.listContent"><a :href="text.link">{{ text.text }}</a></li>
                </ul>
            </div>

        </div>
        <div>
            <img src="../../assets/img/dc-logo-bg.png" alt="">
        </div>
    </div>
</template>
<style scoped lang="scss">
@use "../../style/partials/variable.scss" as *;
@use "../../style/partials/mixin.scss" as *;

div.container {
    background-image: url(../../assets/img/footer-bg.jpg);
    background-size: cover;
    color: $color-text-white;
    @include padding-standard;
    padding-top: 40px;
    padding-bottom: 60px;
    position: relative;
    overflow: hidden;
    min-height: 400px;

    div.content {
        width: 40%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        div.list {
            // width: calc(100% / 3);
            display: flex;
            flex-direction: column;
            gap: 15px;

            li {
                color: gray;
                padding-bottom: 10px;
            }
        }
    }

    img {
        position: absolute;
        top: -20%;
        right: 20%;
    }
}
</style>