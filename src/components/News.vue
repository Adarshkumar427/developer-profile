<script setup>
import shoes from '../assets/shoes.jpg'
import earPhone from '../assets/earPhone.jpg'
import cubes from '../assets/cubes.webp'
</script>
<template>
    <div class="news" id="news">
        <div class="content">
            <h1>LATEST <span style="color: #e54b4b;">NEWS</span></h1>
            <div class="cards">
                <div class="card">
                    <div class="card-img">
                        <img :src="shoes" alt="shoes">
                    </div>
                    <h3>Developer watch out for these burnout symptoms</h3>
                    <p>BY ALEX WATSON / 01 JANUARY 2022</p>
                </div>
                <div class="card">
                    <div class="card-img">
                        <img :src="earPhone" alt="earPhone">
                    </div>
                    <h3>How to be appreciated for your hard work as a developer</h3>
                    <p>BY BOOK KENNEDY / 22 DECEMBER 2021</p>
                </div>
                <div class="card">
                    <div class="card-img">
                        <img :src="cubes" alt="cubes">
                    </div>
                    <h3>How to designers and developers can collaborate better</h3>
                    <p>BY PAOLA ATKINS / 05 DECEMBER 2021</p>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.news {
    background-color: rgb(250, 247, 247);
    ;
}

.content {
    max-width: 1100px;
    margin-inline: auto;
}

h1 {
    padding-block: 50px;
    letter-spacing: 10px;

}

.cards img {
    height: 250px;
    width: 100%;
    border-radius: 5px;
    transition: transform 0.3s ease-in-out;
    /* margin-top: 100px; */
}

.card-img {
    height: 250px;
    overflow: hidden;
    border-radius: 5px;
}

.cards {
    display: flex;
    gap: 50px;
    padding-bottom: 100px;
}

.card h3 {
    padding-top: 20px;
    letter-spacing: 2px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.card {
    overflow: hidden;
    /* height: 250px */
    /* Prevents the image from overflowing */
    /* display: inline-block; */
}

.card p {
    padding-top: 20px;
    letter-spacing: 1px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    color: gray;
}

.card:hover img {
    transform: scale(1.1) rotate(3deg);
}

@media (max-width:1150px) {

    .cards h3,
    p {
        margin-left: 15px;
    }

    .cards {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        margin: 0;
        padding: 0;
    }
}
</style>