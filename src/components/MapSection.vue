<template>
    <section class="map-section">
        <SectionLabel label="Bizi Bulun" />
        <div class="map-frame">
            <div class="map">
                <div id="address">
                    <h3>Varank Fen Lisesi</h3>
                    <i class="fas fa-map-marker-alt"></i>
                    Aydınevler,<br> Saygı Caddesi, <br> No 28, <br> 34854
                    Maltepe/İstanbul<br><br>
                    <iframe
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d96388.89504832272!2d29.01034673353016!3d40.978131105908766!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14cac6880b8786f5%3A0x1da8998bd491da0b!2s%C5%9Eehit%20%C4%B0lhan%20Varank%20Fen%20Lisesi!5e0!3m2!1str!2str!4v1678792565017!5m2!1str!2str"
                        width="250" height="250" style="border:0;" allowfullscreen="" loading="lazy"
                        referrerpolicy="no-referrer-when-downgrade"></iframe>
                    <br>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
import SectionLabel from './SectionLabel.vue';

export default {
    name: 'MapSection',
    components: {
        SectionLabel
    }
}

</script>

<style scoped>
.map-section {
    padding: 2vh 25vw;
    text-align: center;
}

.map {
    display: flex;
    align-items: center;
    justify-content: center;
    padding-bottom: 3vh;
    padding-left: 8vw;
    padding-right: 8vw;
    padding-top: 2vh
}

.map-frame {
    display: inline-flex;
    flex-direction: row;
}



#address {
    position: relative;
    text-align: center;

}

.frame {
    display: flex;
}

@media (max-width: 900px) {

    .map-section {
        padding: 2vh 12vw;
        align-items: center;
    }

    .map {
        display: flex;
        align-items: center;
        padding-bottom: 3vh;
        padding-top: 2vh;

    }


    #address {
        position: relative;
        text-align: center;
        align-items: center;
    }

}

.btn_one {
    font-size: 18px;
    color: #000000;
    background: #ffffff;
    border: 3px solid #000000;
    padding: 8px 40px;
    /*    width: %; */
    border-radius: 80px;
    font-weight: bold;
    margin-top: 50px;
    margin-bottom: 50px;
    margin-left: auto;
    margin-right: auto;
    transition: 0.4s ease-in-out;
    text-decoration: none;
}

.btn_one:hover {
    box-shadow: 0px 10px 30px #111822;
    cursor: pointer;
    color: #ffffff;
    background: #000000;
}

@media (max-width: 1000px) {

    .map-frame {
        display: block;
        flex-direction: row;
    }

    .btn_one {
        padding: 6px 30px;
        width: 50%;
        background: #ffffff;
        color: #000000;
        text-decoration: none;
        text-align: center;
    }

    .btn_one:hover {
        box-shadow: 0px 1px 1px #000000;
        cursor: pointer;
    }
}
</style>