<template>
    <section class="faq-section">
        <div class="faq-warp">
            <div class="container">
                <SectionLabel label="Sıkça Sorulan Sorular" />
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
                question: 'Kanser ve Moleküler Biyoloji Komitesi',
                answer: 'Kesin çözümü bulunamayan kanseri yeryüzünden silebilecek miyiz? Kanser vücudun herhangi bir yerinde hücrelerin düzensiz çoğalmasıyla meydana gelen bir hastalıktır. Şu anda bilinen tedaviler olan radyoterapi, kemoterapi gibi yöntemlerin yetersiz olduğunu ve kanserin geri gelebildiğini biliyoruz. Peki son zamanlarda adını çokça duyduğumuz moleküler biyoloji ve genetik bilimi, kanseri yenmenin bir yolunu bulmuş olabilir mi? Kanserle ilgili günümüz tedavileri, geliştirilebilecek yeni yöntemler ve kanser ile ilgili daha birçok konuyu tartışmak için sizi kanser ve moleküler biyoloji komitemize bekliyoruz!'
            },
            {
                question: 'Adli Bilimler Komitesi',
                answer: 'Adli tıp sadece otopsiden mi ibarettir? Adli bilimler nelerdir, hangi alanlarda çalışır? Geleceğin adli tıbbı ve adli bilimleri nasıl bir şekil alacaktır, ülkemizde bu yeni teknolojilerin uygulanabilirliği nedir? Suçlu bulunana kadar ki süreçte hangi teknikler kullanılır? Suç dünyasının aydınlatıcı yüzü adli tıp ve adli bilimlerin geçmişten geleceğe incelerken farklı yönleriyle de ele alacağız. Otopsinin iç yüzünden, olay yerinde bulunan bulguların değerlendirilme aşamalarına,  adli tıp sahalarında göreceğimiz yeni teknolojilerden bilirkişi raporlarına ve adli tıbbın suçluların bulunmasına katkılarından bahsedeceğiz. Tüm bunları yaparken komite içinde etkinliklere ve gerçek davalardan, dizilerden, filmlerden örneklere bolca yer vereceğiz. Mideniz hassas değilse, biraz da ilginiz varsa komitemize bekleriz.'
            },
            {
                question: 'Psikoloji / Psikiyatri Komitesi',
                answer: 'Komitemizin ilk günü ruhun derinliklerine daldıktan sonra ikinci günü ruhsal hastalıklarla dolu geçireceğiz. Hazır olun, kemerlerinizi takın! Travma, kişinin beklemediği bir olaya sınırlarını zorlayan bir şekilde maruz kalmasıdır. Peki travma neden oluşur? Travma kalıcı mıdır? Travma neden dissosiyasyona yol açar? Bilinçaltı nedir? Bilinçaltımıza neden ulaşamayız? Ruh nedir? Ruhun şematize edilmesi ve incelenmesi, arketipler ve en karmaşık rüyalarımız... Rüyalarımız neden gerçek çıkarlar? Neden rüya görürüz? İkinci günümüzde ise dissosiyatif bozukluklarda yaşanan amneziler, epizodlardan sonra hatırlanamayan anılar hakkında tartıştıktan sonra şizofreninin aydınlatılamamış noktalarında çalışmalar ve tartışmalar üzerinden ilerleyeceğiz. Ayrıca sonrasında travma sonrası stres bozukluğu hakkındaki çalışmalarımız, ilgi çekici vakalarımız ve atölyelerimiz ile komitemiz devam edecek! Psikoloji/psikiyatri komitesinde sizi keyifli ve bilgi dolu günler bekliyor! Her psikoloji aşığını bekliyoruz!'
            },
            {
                question: 'Kara Delik Komitesi',
                answer: 'Uzay zamanı büken, olay ufkuna giren her maddeyi hapseden, astrofizik dünyasının uzun zamandır en merak ettiği konulardan biri olan kara delikleri; iki gün boyunca derinlemesine inceleyeceğiz. Birçok bilim kurgu filmine konu olan, evrendeki en muhteşem ve en gizemli gök çizimlerinin oluşumundaki etkenleri konuşurken aynı zamanda atölye çalışmalarıyla komitemizi daha keyifli bir hale getirmeyi planlıyoruz. Bir kara deliğin içine düşersek ne olur, kara delikler yeni evrenler oluşturabilir mi, kara delikler birer solucan deliği olabilir mi gibi sorulara da cevap arayacağız. Alanında uzman astrofizikçileri konuk edeceğimiz komitemizde kara deliklerin doğumundan ölümüne kadar her evresini teorilerle inceleyeceğiz. Eğer siz de bilimkurgu filmlerini wikipediada araştırmadan izlemek istiyorsanız sizi komitemize bekliyoruz.'
            },
            {
                question: 'Nükleer Enerji Komitesi',
                answer: 'Bir tuşa basıp Dünya\'yı yok etmek mi yoksa bu gücü kontrol altına alıp gezegenin enerji ihtiyacını sağlayıp geleceğimizi garanti altına almak mı\? İkisi de mümkün. İşte bu iki ayrımı da nükleer enerji komitesinde tartışacağız.Dünyamızı saran bu büyük güç; şeytani kullanım alanları olmasına rağmen geleceğimizin kurtarıcısı olarak da görülen nükleer enerji, nükleer enerji santralleri ve nükleer silahlar hakkında her şey bu komitede! Nükleer enerji konusunda yetkin profesörlerimiz ile beraber nükleer enerjinin elde ediliminden her türlü kullanım alanına, yararından zararına, bu zararlara yönelik nasıl önlemler alınabileceğine değinip kullanılmasının gerekliliği konusunda hararetli bir tartışma ortamı yaratacağımız komitemize sizleri bekliyoruz'
            },
            {
                question: 'Kuantum Fizik / Biyoloji Komitesi',
                answer: 'Klasik fiziğin  kurallarını ihlal eden kuantum fiziğinin canlı yaşamında ilgi çekici derecede fazla kesişimleri olduğunu biliyor muydunuz ? Son zamanların en ilginç araştırma alanlarından biri olan kuantum biyolojisini sizlerle beraber inceleyeceğiz. Kuantum ve biyoloji kelimelerinin oluşturduğu önyargınızı kenara bırakmanızı rica ediyoruz çünkü canlılar dünyası ve teorik fiziğin oluşturacağı üst düzey farkındalık ve eğlenceli sohbetten mahrum kalmanızı istemiyoruz. Klasik fiziğin tarihi üzerine kısa bir konuşmanın ardından kuantum fiziği ile ilgilenecek ve karşılaştırmalarını yapacağız. Bu esnada kuantum fiziği üzerine yapılmış tarihi tartışmalara da değinecek ve kendi aramızda da tartışacağız. Her ne kadar soyut bir alan gibi görünse de aslında dünyamızın ısınmasından solunuma, fotosentezden göçmen kuşların yön bulmasına, enzimlerin çalışmasından koku duyusu ve mutasyona kadar birçok alanda kendine yer edinen kuantum fiziğinin bu alanlardaki payını konuşacağız ve yaşam nedir sorusuna cevap arayacağız. Kendiniz gibi arastırmacı genç ruhlarla polemiğe girip kendinize yeni bir ufuk açmak isterseniz bu komite tam size göre!'
            },
            {
                question: 'Kimya Her Yerde',
                answer: 'Komitemizde de kimyanın dokunduğu pek çok alana değineceğiz. İlk gün kimya ve kimya teknolojileri nelerdir, günlük hayatta ve sanayide kullanımı, fabrika robotları, otomasyon, nanoteknoloji, nano coatings, 3D printing nedir ve ne seviyede geliştirilebilir konularına değineceğiz. İkinci gününde UV cruable coatings, ahşap boyaları çeşitleri ve boyanın tarihi gibi daha birçok konuyu konuşurken kullanılan aletleri de kendiniz inceleme fırsatını bulabileceksiniz. İki günde de çok eğlenceli atölye çalışmalarımız, daha bir sürü sürpriz ve aktif katılımcılarımıza hediyelerimiz de olacak. Ayrıca komitemizdeki katılımcılar etkinlik sonrasında “Kayalar Kimya” fabrikasında bir gün geçirmeye ve aletleri, laboratuvarları ve işleyişi görmeye hak kazanacaklar! Sizleri FBÇ’2023 kimya komitemizde ağırlamak için can atıyoruz!'
            }
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