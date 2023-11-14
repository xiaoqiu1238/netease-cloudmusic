<template>
    <div>
        <div class="rec">
            <p class="title"><strong style="font-size: 17px;">{{ title }}</strong><span class="more"
                    style="float: right; font-size: 14px; color: rgb(157, 157, 157);">更多></span></p>

            <ul>
                <li v-for="(value, key) in myObject" :key="key">
                    <img :src="value.imageUrl" alt="">
                    <p class="songTitle">{{ value.songName }}</p>
                    <p class="songInfo">{{ value.songInfo }}</p>
                </li>
            </ul>
        </div>


    </div>
</template>

<script>
export default {
    name: 'RecommendMore',
    data() {
        return {
            myObject: {
                song1: {
                    imageUrl: '',
                    songName: '时间煮雨',
                    songInfo: '张杰'
                },
                song2: {
                    imageUrl: 'path/to/image2.jpg',
                    songName: 'Song 2',
                    songInfo: 'Info about Song 2'
                },
            },
            title: "歌曲推荐"
        }
    },
    props: {

    }
}
</script>

<style>
.rec {
    margin-top: 10px;
}
ul {
            list-style: none;
            padding: 0;
        }

        li {
            
            margin-bottom: 10px;
            padding: 10px;
            display: flex;
            align-items: center;
        }

        img {
            max-width: 100px;
            margin-right: 10px;
        }

        .songTitle {
            font-size: 18px;
            font-weight: bold;
            margin: 0;
        }

        .songInfo {
            margin: 5px 0 0;
            color: #ababab;
        }
</style>