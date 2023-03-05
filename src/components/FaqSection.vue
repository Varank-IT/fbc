<template>
    <section class="faq-section">
        <div class="faq-warp">
            <div class="container">
                <SectionLabel label="Komiteler" />
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
    name: 'FaqSection',
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
        ]
    })
}
</script>

<style scoped>
.faq-section {
    min-height: 100vh;
    min-height: 50vh;
    font-weight: bold;
    text-align: left;
}

.faq-warp {
    /*padding: 6vh 4vw;*/
    padding: 2vh 12vw;
}

.faq {
    background: #FFFFFF;
    box-shadow: 0 2px 48px 0 rgba(0, 0, 0, 0.06);
    border-radius: 4px;
}

@media (max-width: 1000px) {
    .faq {
        margin-bottom: 30px;
    }
}
</style>