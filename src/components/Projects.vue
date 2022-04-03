<template>
    <section id="projects">
        <div class="container">
            <main>
                <h2 class="projects-title">Mes projets</h2>

                <!-- Project 1 -->
                <div class="main-content project-1">
                    <a
                        href="http://pournoobs-frontend.herokuapp.com"
                        target="_blank"
                        class="img-link"
                    >
                        <div class="project-img-container">
                            <img
                                src="@/assets/img/projects/pournoobs.png"
                                class="w-100 project-img project-img-1"
                            />
                        </div>
                    </a>
                    <div class="project-content">
                        <h3 class="project-title">
                            <span class="whity">Pournoobs</span>
                        </h3>
                        <div class="project-description">
                            <p class="project-1-para-1">
                                Une plateforme d'apprentissage en ligne spécialisée dans l'univers de l'e-sport.
                                Cette application web permet à n'importe quel "noob" de monter en compétences sur le gaming, le livestreaming et d'autres domaines et ce, en toute autonomie.
                            </p>
                            <p
                                class="project-1-para-2 mb-0"
                            >La charte graphique reprend celle d'un célèbre site et démontre que l'on peut faire preuve à la fois d'humour et de sérieux en même temps.</p>
                        </div>
                        <ul class="techno-list techno-list-1 list-unstyled d-flex gap-5 mt-3">
                            <li class="whity">Vue.js</li>
                            <li class="whity bootstrap">Bootstrap</li>
                            <li class="whity">Laravel</li>
                            <li class="whity">Heroku</li>
                        </ul>
                    </div>
                    <a href="http://pournoobs-frontend.herokuapp.com" target="_blank">
                        <i class="fa-solid fa-arrow-up-right-from-square link-icon"></i>
                    </a>
                </div>

                <!-- Project 2 -->
                <div class="main-content project-2">
                    <a href="https://aze-couture.com/" target="_blank" class="img-link">
                        <div class="project-img-container">
                            <img
                                src="@/assets/img/projects/azecouture.png"
                                class="w-100 project-img project-img-1"
                            />
                        </div>
                    </a>
                    <div class="project-content">
                        <h3 class="project-title">
                            <span class="whity">Aze Couture</span>
                        </h3>
                        <div class="project-description">
                            <p
                                class="project-1-para-1"
                            >Site e-commerce pour une marque de streetwear à Nantes. Désireuse d'étendre son activité et d'obtenir un canal de vente supplémentaire, la créatrice m'a contacté afin que nous collaborions et lui offrions un outil personnalisé et à l'image de son entreprise.</p>
                            <p
                                class="project-1-para-2 mb-0"
                            >Le thème Wordpress utilisé est "Astra" et les pages ont été construites à l'aide d'Elementor Pro.</p>
                        </div>
                        <ul class="techno-list techno-list-2 list-unstyled d-flex gap-5 mt-3">
                            <li class="whity">Wordpress</li>
                            <li class="whity">Woocommerce</li>
                            <li class="whity">Stripe</li>
                        </ul>
                    </div>
                    <a href="https://aze-couture.com/" target="_blank">
                        <i class="fa-solid fa-arrow-up-right-from-square link-icon"></i>
                    </a>
                </div>
            </main>
        </div>
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.container {
    padding: 200px 0 200px;
}

main {
    text-align: left;
    position: relative;

    .projects-title {
        color: $secondary-color;
        font-size: 2.2rem;
        text-transform: uppercase;
        font-weight: bold;
        text-align: center;
        margin-bottom: 50px;
    }

    .main-content {
        position: relative;
        background: rgba(0, 0, 0, 0.3);
        backdrop-filter: blur(5px) saturate(180%);
        -webkit-backdrop-filter: blur(5px) saturate(180%);
        width: 80%;
        min-height: 500px;
        box-shadow: 0 0 10px rgba(0, 220, 130, 0.1);
        color: $font-color-secondary;
        padding: 80px 50px 50px;
        margin: 0 auto 70px;
        display: flex;

        .project-img-container {
            width: 60%;
            max-width: 700px;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            box-shadow: 0 10px 30px -15px rgba(2, 12, 27, 0.7);
            filter: saturate(80%);

            &:hover {
                filter: saturate(100%);
            }

            &::before {
                content: "";
                width: 100%;
                height: 100%;
                background-color: rgba(0, 220, 130, 0.3);
                position: absolute;
                top: 0;
                left: 0;
                transition: 0.2s ease-in-out;
            }

            &:hover::before {
                background-color: rgba(0, 220, 130, 0);
            }

            .project-img {
                object-fit: cover;
            }
        }

        .project-content {
            max-width: 550px;
            font-family: "DM Sans", sans-serif;

            .project-title {
                font-weight: bold;
            }
        }

        .project-description {
            background: rgba(10, 40, 40, 0.6);
            backdrop-filter: blur(10px) saturate(100%);
            -webkit-backdrop-filter: blur(10px) saturate(100%);
            color: $font-color-secondary;
            padding: 30px;
        }

        .techno-list-1 {
            justify-content: end;
        }

        .techno-list-2 {
            justify-content: start;
        }
    }

    .project-1 {
        text-align: right;
        justify-content: end;

        .project-img-container {
            left: -80px;
        }
    }
    .project-2 {
        text-align: left;
        justify-content: start;

        .project-img-container {
            right: -80px;
        }
    }

    .whity {
        color: $font-color-primary;
    }

    .link-icon {
        position: absolute;
        z-index: 2;
        color: $font-color-primary;
        bottom: 20px;
        right: 20px;

        &:hover {
            color: $secondary-color;
        }
    }
}

@media screen and(max-width: 1200px) {
    .img-link {
        display: none;
    }

    .project-content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%) !important;

        .project-title,
        li {
            text-shadow: 0 0 1px #fff;
        }

        .project-description {
            color: $font-color-primary !important;
        }
    }

    .main-content {
        box-shadow: 0 0 10px rgba(0, 220, 130, 0.6) !important;

        &::before {
            content: "";
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            background: rgba(10, 40, 40, 0.6);
            backdrop-filter: blur(6px) saturate(100%);
            -webkit-backdrop-filter: blur(6px) saturate(100%);
        }
    }

    .project-1 {
        background-image: url("@/assets/img/projects/pournoobs.png") !important;
        background-size: cover !important;
        background-repeat: no-repeat !important;
        background-position: center !important;
    }

    .project-2 {
        background-image: url("@/assets/img/projects/azecouture.png") !important;
        background-size: cover !important;
        background-repeat: no-repeat !important;
        background-position: center !important;
    }
}

@media screen and (max-width: 576px) {
    .project-content {
        width: 340px !important;
        text-align: center;
    }

    .project-title {
        text-align: center !important;
    }

    .techno-list {
        justify-content: center !important;
        gap: 10px !important;
        font-size: 0.9rem;
    }

    .link-icon {
        right: 10px !important;
        bottom: 10px !important;
    }
}
</style>