<template>
    <header class="nav animated slideInDown" :class="{ 'isScrolled': hasScrolled }" style="animation-delay:0.8s;">
        <input type="checkbox" id="nav-check">
        <div class="nav-header">
            <div class="nav-title">
                V | FBÇ
            </div>
        </div>
        <div class="nav-btn">
            <label for="nav-check">
                <span></span>
                <span></span>
                <span></span>
            </label>
        </div>

        <div class="nav-links">
            <a href="https://varankfl.com/fbc/adres" target="_self">Nasıl Gidilir</a>
            <a href="https://varankfl.com/fbc/komiteler" target="_self">Komiteler</a>
            <a href="https://varankfl.com/fbc/galeri" target="_self">Galeri</a>
        </div>
    </header>
</template>

<script>
export default {
    name: 'TheHeader',
    data: () => ({
        hasScrolled: false
    }),
    methods: {
        handleScroll() {
            if (window.innerWidth >= 1) {
                this.hasScrolled = document.body.scrollTop > 60 || document.documentElement.scrollTop > 60;
            }
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.handleScroll);
    }
}
</script>

<style lang="scss" scoped>
header {
    width: 100vw;
    padding-top: 1vh;
    padding-bottom: 1vh;
    position: fixed;
    font-weight: bold;
    background-color: #3d5a99;
    box-shadow: none;
    transition: 0.4s ease-in-out;
    z-index: 2;
    color: #ffffff;
}

header.isScrolled {
    background-color: #ffffff;
    color: #3d5a99;
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.09);
}

.nav>.nav-header {
    display: inline;
}

.nav>.nav-header>.nav-title {
    display: inline-block;
    font-size: 24px;
    padding-left: 2vw;
    padding-top: 10px;
    padding-bottom: 10px;
}

.nav>.nav-btn {
    display: none;
}

.nav>.nav-links {
    display: inline;
    float: right;
    font-size: 18px;
}

.nav>.nav-links>a {
    color: inherit;
    display: inline-block;
    padding-right: 2vw;
    padding-top: 13px;
    padding-bottom: 13px;
    text-decoration: none
}

.nav>.nav-links>a:hover {
    border-bottom: 2px solid #fff;
}

.nav>#nav-check {
    display: none;
}

@media (max-width:1000px) {

    header {
        width: 100%;
        padding-top: 1vh;
        padding-bottom: 1vh;
        position: fixed;
        font-weight: bold;
        background: #3d5a99;
        box-shadow: none;
        transition: 0.4s ease-in-out;
        z-index: 2;
        color: #ffffff;
    }

    header.isScrolled {
        background-color: #ffffff;
        color: #3d5a99;
        box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.15);
    }

    .nav>.nav-header>.nav-title {
        display: inline-block;
        width: 70%;
        padding-left: 6vw;
        font-size: 18px;
    }

    .nav>.nav-btn {
        display: inline-block;
        position: absolute;
        right: 0px;
        margin-top: 10px;
        padding-right: 6vw;
    }

    .nav>.nav-btn>label {
        display: inline-block;

    }

    .nav>.nav-btn>label>span {
        display: block;
        width: 25px;
        height: 10px;
        border-top: 2px solid #BEBEBE;
    }

    .nav>.nav-links {
        position: absolute;
        display: block;
        font-size: 18px;
        width: 100%;
        color: #ffffff;
        background-color: #3d5a99;
        height: 0px;
        transition: all 0.3s ease-in;
        overflow-y: hidden;
        top: 50px;
        left: 0px;
        padding-left: 6vw;
    }

    .nav>.nav-links>a {
        display: block;
        width: 100%;
    }

    .nav>#nav-check:not(:checked)~.nav-links {
        height: 0px;
    }

    .nav>#nav-check:checked~.nav-links {
        height: calc(100vh - 50px);
        overflow-y: auto;
    }
}
</style>