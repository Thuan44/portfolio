  <template>
    <section id="intro_section">
        <div class="container">
            <main>
                <div class="rectangle"></div>
                <div class="main-content">
                    <p class="greetings">Bonjour,</p>
                    <h1 class="main-title">
                        Je suis Cong-Thuan Do.
                        <br />
                        <span>Je suis Développeur Fullstack.</span>
                    </h1>
                    <p class="subtitle">
                        <span>J'aime concevoir et construire</span>
                        des interfaces utilisateurs,
                        des outils digitaux et plus largement
                        des expériences personnalisées.
                    </p>
                    <a href="#contact" class="btn contact-btn">Envie de discuter ?</a>
                </div>
            </main>
        </div>
    </section>
</template>

<script setup>

</script>


<style lang="scss" scoped>
#intro_section {
    min-height: 100vh;
}

.container {
    padding-top: 20px;
}

main {
    text-align: left;
    position: relative;
    padding: 60px;
}

.rectangle {
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(5px) saturate(180%);
    min-width: 285px;
    max-width: 250px;
    height: 500px;
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;
    box-shadow: 0 0 10px rgba(0, 220, 130, 0.1);
}

.main-content {
    position: relative;
    z-index: 2;

    .greetings {
        color: $secondary-color;
        font-family: "Electrolize", sans-serif;
        margin-bottom: 30px;
    }

    h1 {
        color: $font-color-primary;
        font-size: clamp(35px, 5vw, 70px);
        font-weight: 800;
        font-family: "Exo", sans-serif;
        span {
            color: $font-color-secondary;
        }
    }

    .subtitle {
        color: $font-color-secondary;
        margin-top: 20px;
        font-family: "DM Sans", sans-serif;
    }

    .contact-btn {
        border: 1px solid $secondary-color;
        color: $secondary-color;
        font-family: "Electrolize", sans-serif;
        border-radius: 0;
        padding: 10px 20px;
        margin-top: 40px;
        &:hover {
            filter: brightness(110%);
            background-color: rgba(62, 96, 70, 0.3);
        }
    }
}
</style>
