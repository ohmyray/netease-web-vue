<template>
    <div class="nav-container">
        <div class="left">
            <div class="logo">
                <h1>
                    <a href="#">网易云音乐</a>
                </h1>
            </div>
            <div class="nav-top-list">
                <ul>
                    <li v-for="(item, index) in navList">
                        <a href="#">{{ item.title }}</a>
                    </li>
                    <!-- <li>
                        <a href="#">发现音乐</a>
                    </li>
                    <li>
                        <a href="#">我的音乐</a>
                    </li>
                    <li>
                        <a href="#">朋友</a>
                    </li>
                    <li>
                        <a href="#">商城</a>
                    </li>
                    <li>
                        <a href="#">音乐人</a>
                    </li>
                    <li>
                        <a href="#">下载客户端</a>
                    </li>-->
                </ul>
            </div>
        </div>
        <div class="right">
            <div class="search-box">
                <input type="text" placeholder="音乐/视频/电台/用户" />
            </div>
            <div class="user-center">
                <a href="#">创作者中心</a>
            </div>
            <div class="user-icon">
                <a href="#">
                    <img src="../assets/images/icon.jpeg" />
                </a>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
export default defineComponent({
    name: 'HelloWorld',
    setup: () => {
        const navList = [
            { title: '发现音乐', link: '', isMate: '' },
            { title: '我的音乐', link: '', isMate: '' },
            { title: '朋友', link: '', isMate: '' },
            { title: '商城', link: '', isMate: '' },
            { title: '音乐人', link: '', isMate: '' },
            { title: '下载客户端', link: '', isMate: '' },
        ]
        const count = ref(0)
        return { count, navList }
    }
})
</script>
  
<style lang="scss" scoped>
.nav-container {
    display: flex;
    justify-content: space-between;
    background-color: #242424;
    color: #cccccc;
    .left,
    .right {
        display: flex;
    }
    .logo {
        width: 176px;
        height: 70px;
        h1 {
            height: 100%;
            width: 100%;
            a {
                display: block;
                height: 100%;
                width: 100%;
                background: url(../assets/images/topbar.png) no-repeat 9999px;
                background-position: 0 0;
                color: #242424;
            }
        }
    }

    .nav-top-list {
        ul {
            margin-bottom: 0;
            display: inline-flex;
            li {
                height: 70px;
                display: flex;
                justify-items: center;
                align-items: center;
                a {
                    padding: 19px;
                    font-size: 14px;
                    color: #cccccc;
                }
                &:hover {
                    background: #000;
                }
                .active {
                    background: #000;
                }
            }
        }
    }

    .right {
        justify-content: center;
        align-items: center;
        > div {
            margin-right: 14px;
        }
        .search-box {
            height: 32px;
            width: 158px;
            background: url("../assets/images/topbar.png");
            background-color: #fff;
            background-position: 0 -99px;
            border-radius: 32px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            input {
                font-size: 12px;
                line-height: 12px;
                border: none;
                outline: none;
                color: #333;
                width: 80%;
                position: absolute;
                right: 2%;
                &::-webkit-input-placeholder {
                    font-size: 12px;
                    color: #ccc;
                }
            }
        }
        .user-center {
            border-radius: 32px;
            line-height: 30px;
            border: 1px solid #4f4f4f;
            a {
                padding: 0 14px;
                font-size: 12px;
                color: #cccccc;
            }
        }

        .user-icon {
            > a {
                > img {
                    border-radius: 32px;
                    line-height: 32px;
                }
            }
        }
    }
}
</style>
  