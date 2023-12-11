<script>
export default {
    name: "content",
    data() {
        return {
            title: "current series",
            products: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    },
}


</script>
<template>
    <div class="container">
        <div class="jumbotron">

        </div>
        <div class="product">
            <button> {{ title.toUpperCase() }} </button>
            <div v-for="product in products" class="comic">
                <img :src="product.thumb" :alt="product.series">
                <h4>{{ product.series }}</h4>
            </div>
        </div>

    </div>
</template>
<style scoped lang="scss">
@use "../../style/partials/variable.scss" as *;
@use "../../style/partials/mixin.scss" as *;

div.container {
    // @include padding-standard;

    background-color: black;
    color: $color-text-white;

    .jumbotron {
        background-image: url(../../assets/img/jumbotron.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        height: 400px;
        position: relative;

    }

    .product {
        @include padding-standard;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 10px;
        margin: 0 auto;
        padding-top: 55px;
        padding-bottom: 55px;
        position: relative;

        button {
            font-size: 25px;
            all: unset;
            color: #ffffff;
            border: 1px solid #0281f7;
            width: 150px;
            height: 40px;
            text-align: center;
            font-weight: bold;
            cursor: pointer;
            background-color: $color-bar;
            position: absolute;
            top: - 20px;
            left: 200px;

        }

        .comic {
            width: calc((100% / 6) - 20px);

            img {
                width: 100%;
                height: 90%;
                padding: 10px;
                object-fit: cover;
            }
        }
    }

}
</style>