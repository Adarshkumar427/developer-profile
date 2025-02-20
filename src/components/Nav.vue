<script setup>
import { ref } from "vue";
import { onMounted, onUnmounted } from "vue";
const isOpen = ref(false);
const isScrolled = ref(false);
const activeSection = ref("/");
const toggleMenu = () => {
    isOpen.value = !isOpen.value
}

const handleScroll = () => {
    isScrolled.value = window.scrollY > 50 // Change color when scrolling past 50px
};
onMounted(() => {
    window.addEventListener("scroll", handleScroll);
});
onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
});
const setActiveSection = (section) => {
    activeSection.value = section;
};
</script>
<template>
    <div class="nav" :class="{ scrolled: isScrolled }">
        <div class="container">
            <div class="main-nav">
                <h1 style="letter-spacing: 10px;">GRAX</h1>
                <button class="menu-btn" :class="{ scrolled: isScrolled }" @click="toggleMenu">
                    <span v-if="!isOpen">☰</span>
                    <span v-else>✖</span>
                </button>

                <ui class="list" :class="{ open: isOpen }">
                    <li>
                        <a href="/" :class="{ active: activeSection === '/' }" @click="setActiveSection('/')">Home</a>
                    </li>
                    <li>
                        <a href="#about" :class="{ active: activeSection === 'about' }"
                            @click="setActiveSection('about')">About</a>
                    </li>
                    <li>
                        <a href="#portfolio" :class="{ active: activeSection === 'portfolio' }"
                            @click="setActiveSection('portfolio')">Portfolio</a>
                    </li>
                    <li>
                        <a href="#news" :class="{ active: activeSection === 'news' }"
                            @click="setActiveSection('news')">News</a>
                    </li>
                    <li>
                        <a href="#contact" :class="{ active: activeSection === 'contact' }"
                            @click="setActiveSection('contact')">Contact</a>
                    </li>
                </ui>
            </div>
        </div>
    </div>
</template>

<style scoped>
.nav {
    box-shadow: 0px 0px 10px rgba(0, 0, 0, .1);
    position: fixed;
    left: 0;
    right: 0;
    z-index: 10;
}

a {
    text-decoration: none;
    color: white;
}

.scrolled {
    background: white;
    padding: 10px 0;

}

.scrolled h1,
.scrolled .list a {
    color: black;
}

.list a.active,
.scrolled .list a.active {
    color: #e54b4b;

}


.main-nav {
    display: flex;
    justify-content: space-between;
    padding: 25px 0px;
    align-items: center;
    color: white;
}

.list {
    display: flex;
    gap: 40px;
    list-style: none;
    font-size: 20px;
    text-decoration: none;
}

/* Mobile Menu Button */
.menu-btn {
    display: none;
    font-size: 28px;
    background: none;
    border: none;
    color: white;
    cursor: pointer;

}





@media (max-width:1000px) {
    .menu-btn {
        display: block;
        align-items: center;
    }



    .list {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 60px;
        right: 0;
        text-align: center;
        background-color: white;
        width: 100%;
        /* color: blue; */
        margin-top: 13px;
        padding: 20px 0;
    }

    .list.open {
        display: flex;
    }
}

@media (max-width:1000px) {
    .menu-btn.scrolled {
        color: black;
    }

    a {
        color: black;
    }
}
</style>
