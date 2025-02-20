<script setup></script>
<template>
    <div class="footer">
        <div class="content">
            <div class="foot">
                <div style="color: white; font-size: 35px; letter-spacing: 5px;margin-bottom: 20px;">GRAX
                </div>
                <div class="icon">
                    <span class="iconify" data-icon="mdi:facebook"></span>
                    <span class="iconify" data-icon="mdi:twitter"></span>
                    <span class="iconify" data-icon="mdi:globe"></span>
                    <span class="iconify" data-icon="mdi:email"></span>
                </div>
                <div style="color: white;font-size: 16px;margin-top: 20px;">&copy COPYRIGHT 2022 BY MARKETIFY</div>

            </div>
        </div>
    </div>
</template>
<style scoped>
.footer {
    background-color: black;
    padding-block: 100px;

}

.iconify {
    color: white;
    font-size: 24px;
    /* padding-right: px; */
}

.content {
    max-width: 1100px;
    margin-inline: auto;
}

.foot {
    display: flex;
    /* gap: 50px; */
    justify-content: space-between;
    align-items: center;
    height: 100%;
    /* background-color: red; */

}

.icon {
    display: flex;
    gap: 20px;
}

@media (max-width:600px) {
    .foot {
        width: calc(100%-40px);
        display: flex;
        flex-direction: column;
        align-items: center;

    }
}
</style>