<script setup></script>


<template>
    <div class="contact" id="contact">
        <div class="content">
            <h1>GET IN <span style="color: #e54b4b;">TOUCH</span></h1>

            <div class="content1">
                <div class="contact-info">
                    <p style="color: gray; padding-bottom: 30px;">Please fill out the form on this section to contact
                        with me. Or call<br>
                        between 9:00 a.m. and
                        8:00
                        p.m.
                        ET, Monday through Friday.</p>

                    <div class="info"><span class="iconify" data-icon="mdi:map-marker"></span> <strong
                            class="strong">Address:</strong>
                        Brook
                        103,
                        New
                        York, USA</div>
                    <div class="info"><span class="iconify" data-icon="mdi:email"></span> <strong
                            class="strong">Email:</strong>
                        example@gmail.com
                    </div>
                    <div class="info"><span class="iconify" data-icon="mdi:phone"></span> <strong
                            class="strong">Phone:</strong> +77 033
                        442 55 57
                    </div>
                    <div class="info"><span class="iconify" data-icon="mdi:globe"></span> <strong
                            class="strong">Website:</strong>
                        www.myaddress.com
                    </div>
                    <div class="info"><span class="iconify" data-icon="mdi:twitter"></span> <strong
                            class="strong">Twitter:</strong>
                        @twitternickname
                    </div>
                    <div class="info"><span class="iconify" data-icon="mdi:facebook"></span> <strong
                            class="strong">Facebook:</strong>
                        @facebooknickname
                    </div>
                </div>

                <div class="contact-form">
                    <input type="text" placeholder="Name">
                    <input type="email" placeholder="Email">
                    <textarea placeholder="Message"></textarea>
                    <button class="btn">Send Message</button>
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped>
.contact {
    padding-top: 120px;
    padding-bottom: 100px;
}

.content h1 {
    letter-spacing: 7px;
    padding-bottom: 50px;
}

.strong {
    margin-left: 8px;
    letter-spacing: 1px;
    padding-right: 20px;
    color: rgb(27, 27, 27);
    font-size: 17px;
    font-weight: normal
}

.iconify {
    color: rgb(37, 36, 36);
    font-size: 30px;
    padding-top: 10px;
}

.content {
    max-width: 1100px;
    margin-inline: auto;
}

.content1 {
    display: flex;
    gap: 100px;
}

.info {
    padding: 10px;
    padding-right: 4px;
    color: gray;
}

.contact-form {
    display: flex;
    gap: 34px;
    flex-direction: column;
    width: 500px;
}

.contact-form input {
    height: 45px;
    letter-spacing: 1px;
    border-radius: 5px;
    padding: 7px;
    font-size: 15px;
    color: gray;
    border: 1px solid gray;
    outline: none;
}

.contact-form textarea {
    height: 130px;
    letter-spacing: 1px;
    border-radius: 5px;
    padding: 5px;
    font-size: 15px;

    color: gray;
    border: 1px solid gray;
    outline: none;
}

@media (max-width:1115px) {
    .content {
        margin-left: 20px;
    }
}

@media (max-width:800px) {
    .content1 {
        display: flex;
        flex-wrap: wrap;
    }

    .contact-form {
        margin-right: 10px;
    }
}
</style>