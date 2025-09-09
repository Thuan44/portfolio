<template>
    <footer id="footer">
        <div class="container">
            <main>
                <div class="main-content">
                    <a href="#navbar" class="btn back-to-top-btn mb-5">
                        <i class="fa-solid fa-up-long"></i>
                    </a>
                    <p class="signature">
                        <small>&copy; 2025 Cong-Thuan Do — Tous droits réservés.</small>
                    </p>
                </div>
            </main>
        </div>
    </footer>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.container {
    padding: 150px 0 20px;

    .signature {
        color: $font-color-secondary;
    }

    .back-to-top-btn {
        position: relative;
        z-index: 2;
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