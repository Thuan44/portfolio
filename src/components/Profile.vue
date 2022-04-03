<template>
    <section id="profile">
        <div class="container">
            <main>
                <div class="main-content">
                    <h2 class="profile-title">Mon profil</h2>
                    <div class="photo-container">
                        <img src="@/assets/img/profile_pic_transparent.png" class="photo w-100" />
                    </div>
                    <p class="profile-description para-1">
                        Bonjour et bienvenue sur mon site personnel ! Je m'appelle
                        <span
                            class="whity"
                        >Cong-Thuan Do</span>.
                        <br />
                        <br />Titulaire d'un
                        <span class="whity">Master en Stratégie Digitale</span>, j'ai décidé de changer de voie pour
                        me spécialiser dans le développement web. Depuis l'écriture de mon premier "Hello World",
                        je m'épanouie pleinement en tant que
                        <span
                            class="whity"
                        >Développeur Fullstack</span> et suis désormais détenteur des titres professionnels
                        <span
                            class="whity"
                        >Développeur Web & Mobile</span> ainsi que
                        <span class="whity">Concepteur Développeur d'Applications</span>.
                    </p>
                    <p class="profile-description para-3">
                        Mon expérience passée dans la communication digitale représente un atout primordiale dans la
                        compréhension des enjeux auxquels peuvent faire face une entreprise dans la conception de ses applications.
                    </p>
                    <p class="profile-description mb-4">
                        Voici les technologies avec lesquelles j'ai pu travailler
                        récemment :
                    </p>
                    <div class="profile-description para-4 d-flex">
                        <ul class="list-unstyled">
                            <li>
                                <i class="fa-solid fa-terminal"></i> Javascript (ES6+)
                            </li>
                            <li>
                                <i class="fa-solid fa-terminal"></i> Vue.js
                            </li>
                            <li>
                                <i class="fa-solid fa-terminal"></i> Wordpress
                            </li>
                        </ul>
                        <ul class="list-unstyled">
                            <li>
                                <i class="fa-solid fa-terminal"></i> PHP
                            </li>
                            <li>
                                <i class="fa-solid fa-terminal"></i> Laravel
                            </li>
                            <li>
                                <i class="fa-solid fa-terminal"></i> MySQL
                            </li>
                        </ul>
                    </div>
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
    padding: 80px 50px 40px;
    margin: 0 auto;

    .profile-title {
        position: absolute;
        top: -20px;
        left: -45px;
        color: $secondary-color;
        font-size: 2.2rem;
        text-transform: uppercase;
        font-weight: bold;
    }

    .photo-container {
        position: absolute;
        top: -100px;
        right: 100px;
        width: 180px;
        filter: grayscale(30%);

        .photo {
            border-radius: 50%;
        }

        &::after {
            content: "";
            border-radius: 50%;
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
            width: 100%;
            background-color: $secondary-color;
            box-shadow: 0 0 10px rgba(0, 220, 130, 0.3);
            backdrop-filter: blur(10px) saturate(180%);
            opacity: 0.9;
            z-index: -1;
        }
    }

    .profile-description {
        font-family: "DM Sans", sans-serif;
    }

    .whity,
    .para-4 {
        color: $font-color-primary;
    }

    .para-4 {
        gap: 50px;
    }

    .fa-terminal {
        color: $secondary-color;
        font-size: 0.8rem;
        margin-right: 5px;
        opacity: 0.8;
    }
}

@media screen and (max-width: 1200px) {
    .photo-container {
        transform: scale(0.7);
    }
}

@media screen and (max-width: 768px) {
    .photo-container {
        display: none;
    }
}

@media screen and (max-width: 576px) {
    .main-content {
        padding: 40px 20px 30px;
    }

    .profile-title {
        left: -20px !important;
    }

    .para-3 {
        display: none;
    }

    .para-4 {
        gap: 10px !important;
    }
}
</style>