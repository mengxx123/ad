<template>
    <my-page title="广告" :page="page">
        <div class="slogan">广告管理平台</div>
        <div class="re-box" style="width: 250px; height: 160px;" @click="click">
            <img class="img" src="/static/img/nicetool.png">
            <div class="tip">广告</div>
        </div>
    </my-page>
</template>

<script>
    export default {
        data () {
            return {
                articles: [],
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
        },
        mounted() {
            // this.$http.get('/u/news/articles').then(
            //     response => {
            //         let data = response.data
            //         this.articles = data
            //     },
            //     response => {
            //         console.log(response)
            //     })
        },
        methods: {
            click() {
                window.open('http://www.nicetool.net/', '_blank')
            }
        }
    }
</script>

<style lang="scss" scoped>
.slogan {
    font-size: 32px;
    margin-bottom: 16px;
}
.news-list {
    .item {
        margin-bottom: 8px;
    }
    .title {
        color: #333;
    }
}
.re-box {
    position: relative;
    width: 300px;
    height: 300px;
    background-color: #fff;
    border: 1px solid #999;
    cursor: pointer;
    .tip {
        position: absolute;
        left: 0;
        bottom: 0;
        background-color: #eee;
        padding: 2px 4px;
        font-size: 12px;
    }
}
</style>
