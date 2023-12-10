<script>
export default {
    name: "content",
    data() {
        return {
            title: "--> Content goes here <--"
        }
    },
}


</script>
<template>
    <div>
        <h3> {{ title }} </h3>
    </div>
</template>
<style scoped lang="scss">
@use '../../style/variable.scss' as *;

div {
    @include padding-standard;
    padding-top: 55px;
    padding-bottom: 55px;
    background-color: black;
    color: $color-text-white;

    h3 {
        cursor: pointer;
        font-size: 25px;
    }
}
</style>