<template>
    <v-row>
        <v-col cols=12 class='text-center'>
            <v-divider class='mt-10 mb-3' ></v-divider>
            <p class='mb-0 text-center footer-text' v-html="footer_text"></p>
            <p>
            </p>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'AppFooter',
    computed: {
        footer_text: function() {
            if ( this.$store.state.sys.footer != undefined ) {
                return this.$store.state.sys.footer;
            }
            return this.footer;
        },
    },
    data: () => ({
        footer: "本站基于Calibre构建，感谢开源界的力量。所有资源搜集于互联网，如有侵权请邮件联系。",
    })
}
</script>

<style>

</style>
