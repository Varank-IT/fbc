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
        <div class="faq-warp">
            <div class="container">
                <div class="row">
                    <div class="faq">
                        <AccordionItem v-for="(faq, index) in faqs" :key="faq" :info="faq" :badgeNumber="index + 1" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Badge from './accordion/Badge.vue';
import SectionLabel from './SectionLabel.vue'
import AccordionItem from './accordion/AccordionItem.vue';

export default {
    name: 'AboutSection',
    components: {
        Badge,
        SectionLabel,
        AccordionItem
    },
    data: () => ({
        faqs: [
            {
                question: 'Etkinlik nerede olacak?',
                answer: 'Etkinliğimiz okulumuz Şehit İlhan Varank Fen Lisesinde gerçekleşecektir. Adrese sitenin en altından ulaşabilirsiniz.'
            },
            {
                question: 'Etkinlik ne zaman olacak?',
                answer: 'Etkinliğimiz 6-7 Mayıs tarihlerinde gerçekleşecektir.'
            },
            {
                question: 'Komiteler kaç kişilik?',
                answer: 'Her komiteye başvurular arasından 20-25 kişi aralığında katılımcı seçilecektir.'
            },
            {
                question: 'Dresscode olacak mı?',
                answer: 'Evet, dresscode Instagram sayfamız üzerinden duyurulacaktır.'
            },
            {
                question: 'Başvurular ne zaman açılacak?',
                answer: 'En kısa zamanda başvuru formumuz websitemizde olacak ve duyurusu sosyal medya hesabımızdan yapılacaktır!'
            },
            {
                question: 'Komitelere önceden hazırlanmamız gerekiyor mu?',
                answer: 'Komite konuları hakkında önceden araştırma yapmanız tavsiye edilmekle birlikte, sıkı bir hazırlık yapmadığınız surette dahi moderatörlerimizin aktaracakları ve seviyenizde yapılacak tartışmalar sayesinde süreç içerisinde öğrenecekleriniz sonucu komite işleyişinde sorun yaşamazsınız. Gelecek katılımcılar, komite konuları hakkında moderatörlerimiz tarafından önceden araştırabilecekleri ön bilgiler hakkında bilgilendirilecektir. '
            },
            {
                question: 'Komite işleyişi nasıl olacak?',
                answer: 'Her oturum 1.30 saatten oluşmak üzere günde 3 oturum bulunmaktadır. Toplam 6 oturum bulunan etkinliğimizde bu oturumlar moderatörlerimiz tarafından ilgi çekici bilgiler ve tartışma yaratıcı sorularla süregelecektir. Bir veya iki oturumumuz da daha derin bilgiler alabilmek ve komitedeki soruları yanıtlayabilmek için alanında deneyimli uzman kişilerimize ayrılmaktadır. Geri kalan sürelerde de her komite için planlanmış çeşitli deneyler, atölye çalışmaları ve aktivitelerimiz olacaktır.'
            },
        ]
    })
}
</script>

<style scoped>
#bio {
    font-size: 17px;
    margin-left: 25%;
    margin-right: 25%;
    margin-top: 50px;
    word-spacing: normal;
    text-align: center;
}

.sub-h {
    font-size: 30px;
}

.faq-section {
    min-height: 100vh;
    min-height: 20vh;
    font-weight: bold;
    text-align: left;
}

.faq-warp {
    padding: 2vh 25vw;

}

.faq {
    background: #FFFFFF;
    box-shadow: 0 2px 48px 0 rgba(0, 0, 0, 0.06);
    border-radius: 4px;
}

@media (max-width: 1000px) {

    #bio {
        font-size: 17px;
        margin-left: 12%;
        margin-right: 12%;
        margin-top: 50px;
        word-spacing: normal;
        text-align: center;
    }

    .faq {
        margin-bottom: 30px;
    }

    .faq-warp {
        padding: 2vh 6vw;
    }
}
</style>
