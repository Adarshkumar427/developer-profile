<script setup>
import webP2 from '../assets/webP2.webp'
import { Icon } from '@iconify/vue';
</script>
<template>

    <div class="About-sec" id="about">
        <div class="img-sec">

            <img :src="webP2" alt="img">
        </div>
        <div class="content-sec">

            <h1>ABOUT <span style="color:#e54b4b;"> ME</span></h1>
            <p>Hello! I'm Alan Walker. I'm a web developer, and I'm very passionate and dedicated to my work. With
                20
                years experience as a professional web developer, I have acquired the skills and knowledge necessary
                to
                make your project a success. I enjoy every step of the design process, from discussion and
                collaboration.</p>

            <div class="main-list">
                <div class="list">
                    <div style="display: flex; align-items: center;width: 100%; gap: 7px;">
                        <Icon icon="ri:arrow-right-double-line" width="40" height="40" />
                        <span>Web Development</span>
                    </div>
                    <div style="display: flex; align-items: center;width: 100%; gap: 7px;">
                        <Icon icon="ri:arrow-right-double-line" width="40" height="40" />
                        <span>Search Engine Optimization</span>
                    </div>
                </div>
                <div class="list">
                    <div style="display: flex; align-items: center;width: 100%; gap: 7px;">
                        <Icon icon="ri:arrow-right-double-line" width="40" height="40" />
                        <span>Social Media Marketing</span>
                    </div>
                    <div style="display: flex; align-items: center;width: 100%;gap: 7px;">
                        <Icon icon="ri:arrow-right-double-line" width="40" height="40" />
                        <span>Content Generation</span>
                    </div>
                </div>
            </div>

            <button class="btn">Download CV</button>
        </div>

    </div>

</template>
<style scoped>
.About-sec {
    display: flex;
    flex-direction: row;
    gap: 90px;
    margin-top: 100px;
    max-width: 1100px;
    margin-inline: auto;
    width: 100%;
    padding-bottom: 140px;
}





.img-sec img {
    width: 400px;
    height: 457px;
    border-radius: 2px;

}

.content-sec h1 {
    margin-top: 50px;
    letter-spacing: 10px;
}



.content-sec p {
    margin-top: 30px;
    /* letter-spacing: 10px; */
    color: gray;
    word-spacing: 2px;
    line-height: 1.5;
    font-size: 16px;
}


.list {
    display: flex;
    /* gap: 25px; */
}

.main-list {
    margin-top: 20px;
}

@media (max-width:1050px) {
    .About-sec {
        display: flex;
        flex-wrap: wrap;

    }

    .img-sec {
        width: 100%;
    }

    .img-sec img {
        width: 100%;
        margin-left: 5px;
        margin-top: 10px;

    }

    .btn {
        margin-left: 20px;
    }

    .content-sec h1,
    p {
        margin-left: 20px;
    }

    .list {
        margin-left: 12px;
    }
}

@media (max-width:700px) {
    .list {
        flex-wrap: wrap;
    }



}
</style>