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
    padding-top: 60px;
    padding-bottom: 60px;
    background-color: black;
    color: $color-text-white;

    h3 {
        cursor: pointer;
    }
}
</style>