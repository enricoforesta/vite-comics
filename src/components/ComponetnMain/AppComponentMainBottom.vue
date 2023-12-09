<script>
export default {
    name: "MainBottom",
    data() {
        return {
            lists: [
                {
                    title: "DC Comics",
                    listContent: [{
                        text: "testo1",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },
                    {
                        text: "testo4",
                        link: "#"
                    }]
                },
                {
                    title: "DC",
                    listContent: [{
                        text: "testo1",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },
                    {
                        text: "testo4",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },]
                },
                {
                    title: "Sites",
                    listContent: [{
                        text: "testo1",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },
                    {
                        text: "testo4",
                        link: "#"
                    }]
                },
                {
                    title: "Shop",
                    listContent: [{
                        text: "testo1",
                        link: "#"
                    },
                    {
                        text: "testo2",
                        link: "#"
                    },
                    {
                        text: "testo3",
                        link: "#"
                    },
                    {
                        text: "testo4",
                        link: "#"
                    }]
                },

            ]
        }
    },

}
</script>
<template>
    <div class="container">
        <div class="content">
            <div v-for="list in lists" class="list">
                <h3>{{ list.title }}</h3>
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
@use "../../style/variable.scss" as *;

div.container {
    background-image: url(../../assets/img/footer-bg.jpg);
    background-size: cover;
    color: $color-text-white;
    @include padding-standard;
    padding-top: 40px;
    padding-bottom: 60px;
    position: relative;
    overflow: hidden;

    div.content {
        width: calc(100% / 2);
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        div.list {
            width: calc(100% / 3);
            display: flex;
            flex-wrap: wrap;
            flex-direction: column;
            gap: 15px;

            li {
                color: gray;
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