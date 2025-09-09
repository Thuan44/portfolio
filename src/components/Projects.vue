<template>
    <section id="projects">
        <div class="container">
            <main>
                <h2 class="projects-title">Mes projets</h2>

                <!-- Project 1 -->
                <div class="main-content project-1">
                    <a href="https://alif-baa.vercel.app/" target="_blank" class="img-link">
                        <div class="project-img-container">
                            <img src="@/assets/img/projects/alifbaa.png" class="w-100 project-img project-img-1" />
                        </div>
                    </a>
                    <div class="project-content">
                        <h3 class="project-title">
                            <span class="whity">Alif Baa</span>
                        </h3>
                        <div class="project-description">
                            <p class="project-1-para-1">
                                Cette plateforme permet à n’importe qui, même sans aucune base, d’apprendre à
                                lire l’alphabet arabe de façon simple et progressive. Grâce à un mode entraînement
                                interactif et un mode quiz ludique, les utilisateurs peuvent assimiler chaque lettre à leur
                                rythme, tester leurs connaissances et suivre leur progression.
                            </p>
                            <p class="project-1-para-2 mb-0">Une solution idéale pour débuter l’apprentissage de la langue
                                arabe en toute autonomie.</p>
                        </div>
                        <ul class="techno-list techno-list-1 list-unstyled d-flex gap-5 mt-3">
                            <li class="whity">React</li>
                            <li class="whity bootstrap">Zustand</li>
                            <li class="whity">Tailwind CSS</li>
                        </ul>
                    </div>
                    <a href="https://alif-baa.vercel.app/" target="_blank">
                        <i class="fa-solid fa-arrow-up-right-from-square link-icon"></i>
                    </a>
                </div>

                <!-- Project 2 -->
                <div class="main-content project-2">
                    <a href="https://ai-resume-analyzer-nine-nu.vercel.app/" target="_blank" class="img-link">
                        <div class="project-img-container">
                            <img src="@/assets/img/projects/resumind.jpg" class="w-100 project-img project-img-1" />
                        </div>
                    </a>
                    <div class="project-content">
                        <h3 class="project-title">
                            <span class="whity">Resumind</span>
                        </h3>
                        <div class="project-description">
                            <p class="project-1-para-1">Cet outil permet à tout candidat de charger son CV et de
                                le comparer à une offre d’emploi pour en obtenir un score ATS. En quelques secondes et grâce
                                à l’intelligence artificielle de Puter, il analyse la pertinence du CV par rapport aux
                                mots-clés, aux compétences et aux exigences du poste ciblé.
                            </p>
                            <p class="project-1-para-2 mb-0">Un moyen simple, rapide et autonome d’optimiser sa candidature
                                et de maximiser ses chances de passer les filtres automatisés des recruteurs.</p>
                        </div>
                        <ul class="techno-list techno-list-2 list-unstyled d-flex gap-5 mt-3">
                            <li class="whity">React</li>
                            <li class="whity">Tailwind CSS</li>
                            <li class="whity">Puter</li>
                        </ul>
                    </div>
                    <a href="https://ai-resume-analyzer-nine-nu.vercel.app/" target="_blank">
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
            background: rgba(10, 40, 40, 0.4);
            backdrop-filter: blur(1px) saturate(120%);
            -webkit-backdrop-filter: blur(1px) saturate(120%);
        }
    }

    .project-1 {
        background-image: url("@/assets/img/projects/pournoobs.png") !important;
        background-size: cover !important;
        background-repeat: no-repeat !important;
        background-position: center !important;
    }

    .project-2 {
        background-image: url("@/assets/img/projects/nea_lissage_pro.png") !important;
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
        text-shadow: 0 0 1px rgba(0, 220, 130, 0.2) !important;
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