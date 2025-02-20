<script setup>
import Fruit from '../assets/Fruit.jpg'
import brand from '../assets/brand.webp'
import iceCream from '../assets/iceCream.webp'
import cherry from '../assets/cherry.webp'
import coffee from '../assets/coffee.avif'
import Lemon from '../assets/Lemon.webp'
</script>
<template>
    <div class="Portfolio" id="portfolio">


        <div class="content">
            <h1>SELECTED <span style="color:#e54b4b">WORKS</span></h1>


            <div class="grid">
                <img :src="Fruit" alt="fruit">
                <img :src="brand" alt="brand">
                <img :src="iceCream" alt="iceCream">
                <img :src="coffee" alt="coffee">
                <img :src="Lemon" alt="">
                <img :src="cherry" alt="">
            </div>
        </div>

    </div>


</template>
<style scoped>
.Portfolio {
    margin-inline: auto;
    width: 100%;
    /* max-width: 1150px; */
    padding: 0;
    background-color: rgb(250, 247, 247);
}

.content {
    max-width: 1100px;
    margin-inline: auto;
}


h1 {
    padding-top: 30px;
    letter-spacing: 10px;
    margin-top: 100px;
}



img {
    width: 100%;
    display: block;
    object-fit: cover;
    height: 305px;
    border-radius: 10px;

}


.grid {
    margin-inline: auto;
    margin-top: 100px;
    line-height: 0;
    display: grid;
    grid-template-columns: repeat(3, minmax(250px, 1fr));
    gap: 30px;
    padding-bottom: 100px;
}

.grid img:hover {
    opacity: 0;
    transition: 0.3s;
    cursor: pointer;
}

@media (max-width:900px) {
    .grid {
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    }
}

@media (max-width:1100px) {
    .content {
        margin-left: 15px;
        margin-right: 15px;
    }
}
</style>