<script>
import AppComponentLogoDc from './AppComponentLogoDc.vue';
export default {
    name: "navbar",
    data() {
        return {
            menu: [
                {
                    title: "characters",
                    link: "home",
                },
                {
                    title: "comics",
                    link: "home",
                },
                {
                    title: "movies",
                    link: "home",
                },
                {
                    title: "tv",
                    link: "home",
                },
                {
                    title: "games",
                    link: "home",
                },
                {
                    title: "collectibles",
                    link: "home",
                },
                {
                    title: "videos",
                    link: "home",
                },
                {
                    title: "fans",
                    link: "home",
                },
                {
                    title: "news",
                    link: "home",
                },
                {
                    title: "shop",
                    link: "home",
                },
            ]
        }
    },
    components: {
        AppComponentLogoDc
    }
}
</script>

<template>
    <div class="navbar">
        <div class="logo">
            <AppComponentLogoDc />
        </div>
        <div class="list">
            <ul>
                <li v-for="li in menu">
                    <a :href="li.link">{{ li.title.toUpperCase() }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use'../../style/partials/mixin.scss' as *;
@use'../../style/partials/variable.scss' as *;

.navbar {
    display: flex;
    justify-content: space-between;
    @include padding-standard;
    padding-top: 15px;
    font-size: 12px;

    .logo {
        padding-bottom: 15px;
    }

    .list {
        display: flex;
    }

    ul {
        display: flex;
        gap: 15px;
    }

    li {
        height: 100%;
        display: flex;
        align-items: center;

        a:hover {
            color: $color-bar;

        }

        &:hover,
        &:active {
            border-bottom: 2px solid $color-bar ;
        }

    }
}
</style>