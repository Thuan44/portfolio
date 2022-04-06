<template>
    <section id="contact">
        <div class="container">
            <main>
                <div class="main-content">
                    <h2 class="contact-title">Dites bonjour !</h2>
                    <p class="contact-description text-center mb-0">
                        Je suis toujours à l'écoute de nouvelles opportunités.
                        <br />Si mon profil vous intéresse ou si vous souhaitez simplement échanger, je reste disponible par mail.
                    </p>
                    <p class="email">congthuan.do@gmail.com</p>
                </div>
            </main>
        </div>
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.container {
    padding: 200px 0 250px;
}

main {
    text-align: left;
    position: relative;
}

.main-content {
    position: relative;
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(5px) saturate(180%);
    width: 80%;
    box-shadow: 0 0 10px rgba(0, 220, 130, 0.1);
    color: $font-color-secondary;
    padding: 50px 50px 30px;
    margin: 0 auto;

    .contact-title {
        position: absolute;
        top: -20px;
        left: 50%;
        transform: translateX(-50%);
        color: $secondary-color;
        font-size: 2.2rem;
        text-transform: uppercase;
        font-weight: bold;
    }

    .email {
        position: absolute;
        bottom: -100px;
        left: 50%;
        transform: translateX(-50%);
        font-family: "Electrolize", sans-serif;
        color: $secondary-color;
        font-size: 1.5rem;
        text-shadow: 0 0 10px rgba(0, 220, 130, 0.15);
    }
}

@media screen and (max-width: 992px) {
    .contact-title {
        text-align: center;
        width: 300px;
    }
    .main-content {
        padding: 40px 20px 30px;
    }
}
</style>