<script setup lang="ts">
import Card from "../components/AppCard.vue";
import { useRouter } from 'vue-router';
const router = useRouter();
</script>
    
<template>
    <div class="welcome">
        <div>--&nbsp;Welcome&nbsp;To&nbsp;--</div>
        <div>
            <img class="avatar" src="https://images.drshw.tech/images/notes/标准头像.jpg" alt="">
            DrSHW's&nbspLabotory
        </div>
    </div>
    <div class="description">
        天天摸鱼的前端&爬虫，偶尔开展一些奇妙的实验。
    </div>
    <ul role="list" class="link-card-grid">
        <Card class="item" href="https://docs.drshw.tech/main/introduction" title="Library"
            body="DrSHW的图书馆，存放笔记、教程和一些小项目。" />
        <Card class="item" href="https://storage.drshw.tech/" title="Dungeon" body="DrSHW的地下室，云盘而已。其中会包含一些常用的软件。" />
        <Card class="item" href="https://github.com/DrSHW/" title="Github" body="DrSHW的Github。" />
        <Card class="item" @click="router.push('/links')" title="Friends" body="友链。" />
    </ul>
</template>
    
<style lang="scss">
@media (max-width: 768px) {
    .link-card-grid {
        margin: auto;
        margin-top: 5vh;
        position: relative;
        padding: 1em;
        font-family: system-ui, sans-serif;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 1rem;
        width: 95vw;
        justify-content: center;
        align-items: center;
        z-index: 11;
        padding: 0;

        .item {
            height: 22vmax;
            width: 18vmax;
        }
    }

    .welcome {
        position: relative;
        z-index: 10;
        display: flex;
        flex-direction: column;
        width: 100vw;
        align-items: center;
        font-size: 2rem;
        color: transparent;
        text-shadow:
            0px 0px 1px rgba(255, 255, 255, .9),
            0px 4px 4px rgba(0, 0, 0, .05);
        letter-spacing: .2rem;
        margin-top: 2vh;

        .avatar {
            height: 2rem;
            border-radius: 50%;
        }
    }

    .description {
        margin-top: 4vh;
        color: aliceblue;
        font-size: 1.3rem;
        text-align: center;
        margin-left: 3vmax;
        margin-right: 3vmax;
    }
}

@media (min-width: 768px) {
    .link-card-grid {
    margin: auto;
    margin-top: 5vh;
    position: relative;
    padding: 1em;
    font-family: system-ui, sans-serif;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1rem;
    width: 60vw;
    justify-content: center;
    align-items: center;
    z-index: 11;
    padding: 0;
    
    .item {
        cursor: pointer;
        margin-top: 2vh;
        height: 20vh;
        width: 20vw;
        margin-left: 3vh;
        margin-right: 3vh;
    }
}
.welcome {
    position: relative;
    z-index: 10;
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
    font-size: 5rem;
    color: transparent;
    text-shadow:
        0px 0px 1px rgba(255, 255, 255, .9),
        0px 4px 4px rgba(0, 0, 0, .05);
    letter-spacing: .2rem;
    margin-top: 2vh;
    .avatar {
        height: 5rem;
        border-radius: 50%;
    }
}
.description {
    margin-top: 4vh;
    color: aliceblue;
    font-size: 2rem;
    text-align: center;
}
}
</style>
    
