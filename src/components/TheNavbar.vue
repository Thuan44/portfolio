<template>
    <nav id="navbar" class="navbar navbar-expand-md">
        <div class="logo-menu container-fluid">
            <a href="#">
                <div class="logo-container ms-4">
                    <img src="@/assets/img/ctd_logo_transparent.png" class="w-100" />
                </div>
            </a>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="list-unstyled menu mb-0 navbar-nav ms-auto">
                    <li>
                        <a href="#profile" class="link-item">Profil</a>
                    </li>
                    <li>
                        <a href="#experiences" class="link-item">Expériences</a>
                    </li>
                    <li>
                        <a href="#projects" class="link-item">Projets</a>
                    </li>
                    <li>
                        <a href="#contact" class="link-item">Contact</a>
                    </li>
                    <li>
                        <a
                            class="btn cv-btn"
                            href="@/assets/CV_Cong-Thuan_DO_FS.pdf"
                            download
                        >Télécharger CV</a>
                    </li>
                </ul>
            </div>
        </div>
        <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
        >
            <i class="fa-solid fa-bars"></i>
        </button>
    </nav>
</template>

<script setup>

</script>

<style lang="scss" scoped>
nav {
    color: $font-color-primary;
    padding: 20px;
    font-family: "Electrolize", sans-serif;
    z-index: 1;

    .logo-container {
        width: 80px;
    }

    .menu {
        display: grid;
        grid-template-columns: 100px 100px 100px 100px 140px;
        grid-gap: 10px;
        align-items: center;
        justify-items: center;
        justify-content: center;
        padding: 2px 0;
    }

    .navbar-toggler {
        color: #fff !important;
        position: absolute;
        top: 20px;
        right: 20px;
    }

    li {
        position: relative;
    }

    a {
        color: $font-color-primary;
        text-decoration: none;
    }

    a:before,
    a:after {
        content: "";
        position: absolute;
        border-radius: 50%;
        transform: scale(0);
        transition: 0.2s ease transform;
    }

    a:before {
        top: -5px;
        left: -16px;
        width: 6px;
        height: 6px;
        background-color: $secondary-color;
    }

    a:after {
        top: 0px;
        left: -8px;
        width: 4px;
        height: 4px;
        background-color: $font-color-secondary;
    }

    a:hover {
        color: $secondary-color;
    }

    .link-item:hover:before,
    .link-item:hover:after {
        transform: scale(1);
    }

    .cv-btn {
        border: 1px solid $secondary-color;
        color: $secondary-color;
        font-family: "Electrolize", sans-serif;
        border-radius: 0;
        padding: 5px 10px;
        &:hover {
            filter: brightness(110%);
            background-color: rgba(62, 96, 70, 0.3);
        }
    }
}

@media screen and (max-width: 768px) {
    .navbar-collapse {
        margin-top: 20px;
    }
    .menu {
        display: flex !important;
        flex-direction: column;
        align-items: end !important;
        justify-content: end;
        justify-items: end;
    }
}
</style>