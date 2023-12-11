<script>
export default {
    name: "Footer"
}
</script>
<template>
    <div class="footer">
        <button>SING-UP NOW!</button>
        <div class="follow">
            <h4>FOLLOW US</h4>
            <a href="#"><img src="../../assets/img/footer-facebook.png" alt=""></a>
            <a href="# "><img src="../../assets/img/footer-twitter.png" alt=""></a>
            <a href="#"><img src="../../assets/img/footer-youtube.png" alt=""></a>
            <a href="#"><img src="../../assets/img/footer-pinterest.png" alt=""></a>
            <a href="#"><img src="../../assets/img/footer-periscope.png" alt=""></a>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use "../../style/partials/variable.scss" as *;
@use "../../style/partials/mixin.scss" as *;

div.footer {
    height: 110px;
    @include padding-standard;
    display: flex;
    justify-content: space-between;
    align-items: center;

    button {
        all: unset;
        color: $color-text-white;
        border: 1px solid $color-bar;
        width: 150px;
        height: 50px;
        text-align: center;
        font-weight: bold;
        cursor: pointer;
    }

    .follow {
        display: flex;
        align-items: center;
        gap: 20px;

        h4 {
            color: $color-bar;
        }
    }
}
</style>