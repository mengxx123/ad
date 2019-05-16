<template>
    <my-page title="简讯" :page="page">
        <img class="qrcode" src="/static/img/qrcode.jpg" />
        <div class="text">打开微信扫一扫，进入小程序</div>
    </my-page>
</template>

<script>
    export default {
        data () {
            return {
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'apps',
                            href: 'https://app.yunser.com/',
                            target: '_blank',
                            title: '应用'
                        }
                        // {
                        //     type: 'icon',
                        //     icon: 'help',
                        //     to: '/help'
                        // }
                    ]
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
.qrcode {
    display: block;
    width: 160px;
    height: 160px;
    margin: 80px auto 16px auto;
}
.text {
    text-align: center;
    color: #999;
}
</style>
