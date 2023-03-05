<template>
    <section class="bio-section">
        <div id="bio">
            <SectionLabel label="Etkinlik Hakkında" />
            <h2 class="sub-h">Misyonumuz</h2>
            <p>
                Hayallerinin peşinden gitmek isteyen her öğrenciyi; konusunda uzmanlaşmış kişiler ve idealleri olan gençler
                ile bir araya getirerek çeşitli atölye çalışmalarıyla yeteneklerini pekiştiriyor ve tecrübe kazandırıyor,
                tartışma ve yorumlama becerilerini geliştirerek ilgilendikleri fen bilimleri alanında kendilerini keşfetme
                imkanı sunuyoruz.
            </p>
            <h2 class="sub-h">Vizyonumuz</h2>
            <p>
                Lise dönemindeki gençlerimizi fen bilimleri alanlarında uzmanlaşmış kişilerle buluşturup çeşitli projelerle
                kendilerini geliştirmelerini sağlayarak toplumumuza iletişim, problem çözme, yenilikçi düşünme becerisi
                yüksek idealist bireyler kazandırmak vizyonumuzdur.
            </p>
        </div>
    </section>
</template>

<script>
import SectionLabel from './SectionLabel.vue'

export default {
    name: 'AboutSection',
    components: {
        SectionLabel
    }
}
</script>

<style scoped>
#bio {
    font-size: 20px;
    margin-left: 12%;
    margin-right: 12%;
    margin-top: 50px;
    word-spacing: normal;
    text-align: center;
}

.sub-h {
    font-size: 30px;
}
</style>
