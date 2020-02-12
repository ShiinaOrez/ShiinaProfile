<!-- 社交 -->

<template>
    <div class="social" :style="{'font-size': size + 'em'}">
        <!-- github -->
        <a :style="{color: color}" :href="social['github'] || 'https://github.com/ShiinaOrez'" target="_blank"><a-icon type="github" /></a>
        <!-- 微信 -->
        <a-popover arrowPointAtCenter>
            <template slot="content"><img style="width: 360px; max-width: 80vw; height: auto;"  alt="Shiina Orez" src="../../assets/wechat.jpg"/></template>
            <a :style="{color: color}"><a-icon type="wechat" /></a>
        </a-popover>
        <!-- twitter -->
        <a :style="{color: color}" :href="social['twitter'] || 'https://twitter.com/shiina_orez'" target="_blank"><a-icon type="twitter" /></a>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import {mapGetters} from 'vuex';

    @Component({
        components: {
        },
        props: {
            color: String,
            size: Number,
        },
        computed: {
            ...mapGetters(['social']),
        },
    })
    export default class Social extends Vue {
    }
</script>

<style scoped lang="scss">
    .social {
        &>* {
            margin: 0.5em;
        }
    }
</style>

