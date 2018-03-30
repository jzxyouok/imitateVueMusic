<template>
    <div class="m-header">
        <div class="icon"></div>
        <h1 class="text">Chicken Music</h1>
    </div>
</template>

<script type="text/ecmascript-6">
    export default {
    
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
    @import "~common/stylus/variable"
    @import "~common/stylus/mixin"

    .m-header
        position relative
        height 44px
        font-size 0
        color $color-theme
        text-align center
        .icon 
            display inline-block
            margin 6px 9px 0 0
            width 30px
            height 32px
            vertical-align top
            bg-image('logo')
            background-size 30px  32px
        .text
            display inline-block
            line-height 44px
            font-size $font-size-large
            vertical-align top

</style>


