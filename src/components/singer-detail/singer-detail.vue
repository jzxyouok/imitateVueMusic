<template>
    <transition name="slide">
        <div class="singer-detail"></div>
    </transition>
</template>

<script type="text/ecmascript-6">
    import {mapGetters} from 'vuex'
    import {getSingerDetail} from 'api/singer'
    import {ERR_OK} from 'api/config'

    export default {
        computed: {
            ...mapGetters([
                'singer'
            ])
        },
        created() {
            console.log(this.singer.id);
            this._getDetail(this.singer.id)
        },
        methods: {
            _getDetail(id) {
                getSingerDetail(id).then((res) => {
                    if (res.code === ERR_OK) {
                        //console.log(res)
                    }
                }) 
            }
        }
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
    @import "~common/stylus/variable"

    .singer-detail
        position fixed
        top 0
        right 0
        bottom 0
        left 0
        z-index 100
        background $color-background

    .slide-enter-active, .slide-leave-active 
        transition all 0.3s
    .slide-enter, .slide-leave-to
        transform translate3d(100%, 0, 0)
</style>
