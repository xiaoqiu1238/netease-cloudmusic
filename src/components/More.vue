<template>
    <div>
        <div class="rec">
            <p class="title"><strong style="font-size: 17px;">{{ title }}</strong><span class="more"
                    style="float: right; font-size: 14px; color: rgb(157, 157, 157);">更多></span></p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'RecommendMore',
    data() {
        return {
            title: "歌曲推荐"
        }
    },
    props: {

    }
}
</script>

<style>
.rec{
    margin-top: 10px;
}
</style>