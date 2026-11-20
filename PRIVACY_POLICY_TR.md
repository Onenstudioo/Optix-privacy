# Optix Gizlilik Politikası

**Son güncelleme:** 20 Kasım 2026  
**Uygulama sürümü:** 1.4.3  
**Geliştirici:** OnenStudioo  
**İletişim:** onenstudioo@gmail.com

Optix, Android telefonlarda ön kamerayı kullanarak kamera görüntüsünde birden fazla yüz bulunduğunda kullanıcıya uyarı vermek için tasarlanmış bir ekran gizliliği yardımcı uygulamasıdır. Optix yüz sayar; kişileri tanımaz veya kimliklerini belirlemez, biyometrik kimlik doğrulama yapmaz, göz hareketlerini ya da bir kişinin ekrana bakıp bakmadığını ölçmez. Algılama sonucu, başka bir kişinin ekranınızı gördüğünün kesin kanıtı değildir ve yanlış/eksik algılama olabilir.

## 1. Kısa özet

- Kamera kareleri Optix tarafından cihaz üzerinde analiz edilir; Optix bunları fotoğraf veya video olarak kaydetmez, kendi sunucularına yüklemez ve paylaşmaz.
- Optix'in hesap, reklam, profil oluşturma veya kendi analitik/izleme sistemi bulunmaz.
- Optix konum, mikrofon, rehber veya dosya/depolama erişimi talep etmez.
- İstatistikler ve uygulama tercihleri cihazda, uygulamaya özel yerel alanda saklanır.
- Kamera koruması kullanıcı tarafından başlatılır. Telefon açıldığında veya uygulama açılır açılmaz kamera kendiliğinden başlatılmaz.

## 2. Kamera ve yüz algılama

Kamera izni, ön kameradan görüntü almak ve yüz sayısını belirlemek amacıyla kullanılır. Koruma başlatıldığında kamera, görünür Android kamera göstergesi ve Optix'in devam eden bildirimini içeren kamera türündeki ön plan hizmeti üzerinden çalışabilir; böylece koruma başka uygulamalara geçildiğinde de devam edebilir. Kullanıcı korumayı uygulamadan veya hizmet bildiriminden durdurabilir.

Görüntüler CameraX ve Google ML Kit yüz algılama bileşenleriyle cihazda, analiz için gereken süre boyunca bellekte işlenir. Optix görüntüleri dosyaya kaydetmez, yüz görüntüsü/şablonu/kimliği oluşturup saklamaz ve görüntüleri kendi sunucusuna iletmez. Telefon kilitlendiğinde kamera koruması askıya alınır ve kamera serbest bırakılır. Kamera izninin kaldırılması, kamera gizlilik anahtarının kapalı olması, kameranın başka uygulaca kullanılması veya Android'in hizmeti durdurması analiz akışını kesebilir.

Optix yüz algılama sonuçlarını yalnızca koruma ve uyarı mantığı için kullanır. Yüz sayımı her koşulda doğru olmayabilir; uzak, kısmen görünür, hareketli, düşük ışıklı veya kameraya dönük olmayan yüzler algılanmayabilir. Uyarı, ekrana bakan bir kişinin varlığını veya gizliliğin ihlal edildiğini kesin olarak göstermez.

## 3. Adaptif tarama

Adaptif tarama açıkken Optix, cihaz üzerinde o an algılanan yüz sayısına göre analiz sıklığını ayarlayabilir. Bu karar için Optix pil durumunu okumaz. Anlık yüz sayısı analiz sürecinde kullanılır; bir yüz profili veya geçmişi oluşturmak için kaydedilmez ve Optix tarafından gönderilmez.

## 4. Cihazda saklanan bilgiler

Optix'in yerel istatistik özelliği aşağıdaki sınırlı bilgileri saklayabilir:

- ikinci yüz uyarılarının toplam ve gün bazında sayısı,
- koruma oturumu sayısı ve toplam koruma süresi,
- son uyarının zamanı,
- uygulama tercihleri (dil, uyarı sesi, ses açık/kapalı, titreşim ve deseni, algılama seçenekleri, adaptif tarama ve seyahat önerisi tercihi gibi),
- seyahat önerisi özelliği açıksa bu tercihin durumu ve önerinin son gösterim zamanı.

Bu kayıtlar uygulamanın yerel, uygulamaya özel saklama alanında tutulur; Optix'in sunucusuna gönderilmez. Kamera görüntüleri, yüz görüntüleri, yüz şablonları, kimlik bilgileri, konum veya seyahat rotası geçmişi bu istatistikler kapsamında tutulmaz.

**Silme:** İstatistikler ekranındaki **İstatistikleri sıfırla** işlemi istatistik kayıtlarını siler/sıfırlar; uygulama tercihlerini sıfırlama anlamına gelmez. Uygulamanın tüm yerel verilerini kaldırmak için Android sistem ayarlarından Optix'in uygulama verilerini temizleyebilir veya uygulamayı kaldırabilirsiniz.

## 5. Bildirimler ve Hızlı Ayarlar

Optix koruma sırasında devam eden hizmet bildirimi, ikinci yüz uyarısı ve seyahat önerisi özelliği etkinleştirilmişse öneri bildirimi gösterebilir. Bildirim içeriği seçtiğiniz uyarı görünürlüğü ayarına göre azaltılabilir. Android bildirim izni ve bildirim kanalı ayarları bu davranışı etkiler.

Android Hızlı Ayarlar panelindeki Optix kutucuğu korumayı başlatma/durdurma kısayoludur. Kutucuk, koruma durumunu yönetmek için kullanılır; ek bir profil veya veri toplama işlevi değildir.

## 6. “Yola çıkınca öner” özelliği (isteğe bağlı)

Bu özellik varsayılan olarak kapalıdır. Kullanıcı açtığında Optix, araçta olma/geçiş durumunu anlamak için Google Play Hizmetleri'nin Activity Recognition (etkinlik tanıma) özelliğini kullanır ve Android sürümüne bağlı olarak **Fiziksel etkinlik** izni ister. Algılanan araç hareketi bir öneri bildirimi göstermek için kullanılır; Optix korumayı otomatik başlatmaz. Konum izni istenmez. Optix hareket, araç veya yolculuk geçmişi tutmaz; özellik tercihini ve önerinin son gösterim zamanını yerel olarak saklayabilir. Özellik Ayarlar'dan kapatılabilir ve izin Android ayarlarından geri alınabilir. Telefon yeniden başlatıldığında veya uygulama güncellendiğinde, özellik açıksa etkinlik tanıma aboneliği yenilenebilir; bu, kameranın açılışta başlatıldığı anlamına gelmez.

Etkinlik tanıma, Google Play Hizmetleri tarafından sağlanır. Google'ın bu hizmetle ilgili veri işlemesi Google'ın kendi politika ve açıklamalarına tabidir.

## 7. İzinler

Optix Android'de aşağıdaki izinleri/servis yeteneklerini kullanabilir:


- **Kamera:** Kullanıcı korumayı başlattığında ön kameradan görüntü alıp cihazda yüz saymak.
- **Bildirimler:** Koruma hizmeti, uyarılar ve isteğe bağlı seyahat önerisini bildirmek (Android 13 ve sonrası izin isteyebilir).
- **Kamera türü ön plan hizmeti:** Koruma açıkken kamera kullanımını görünür biçimde sürdürmek.
- **Titreşim:** Kullanıcı etkinleştirmişse uyarı titreşimi vermek.
- **Fiziksel etkinlik / etkinlik tanıma:** Yalnızca isteğe bağlı “Yola çıkınca öner” özelliği için.
- **Telefon açılışını algılama:** Yalnızca “Yola çıkınca öner” açıkken etkinlik tanıma aboneliğini yenilemek için; kamerayı başlatmak için kullanılmaz.

Optix mikrofon, konum, kişiler veya dosya/depolama izni talep etmez. İzinler Android ayarlarından geri alınabilir; ilgili izin olmadan özellik çalışmayabilir.

## 8. Üçüncü taraf bileşenler ve hizmetler

Optix, yüz algılama için **Google ML Kit** ve isteğe bağlı hareket/etkinlik algılama için **Google Play Hizmetleri** kullanır. Yüz algılama modeli cihazda çalışır. Google'ın SDK ve hizmetleri, hizmetlerini sunmak, güvenilirlik ve performansı ölçmek veya teknik sorunları teşhis etmek için kendi kapsamlarında teknik bilgi/diagnostik verileri işleyebilir. Bu işlemler Optix'in kontrolünde değildir ve ilgili Google politikalarına tabidir. Optix kamera karelerini Google'a veya başka bir üçüncü tarafa göndermek amacıyla tasarlanmamıştır.

- Google Gizlilik Politikası: https://policies.google.com/privacy
- ML Kit Android veri açıklaması: https://developers.google.com/ml-kit/android-data-disclosure

Optix'in kendi reklam ağı, analitik SDK'sı, kullanıcı hesabı, sunucusu veya veri broker entegrasyonu bulunmaz.

## 9. Veri paylaşımı, satış ve güvenlik

Optix kullanıcı verilerini satmaz veya reklam amacıyla profillemez. Optix tarafından oluşturulan yerel istatistikler ve tercihler üçüncü taraflara Optix tarafından aktarılmaz. Kamera verileri Optix tarafından ağ üzerinden iletilmez. Yerel veriler Android'in uygulama izolasyonu içinde saklanır; cihazınıza erişimi olan kişiler, cihaz güvenliği/işletim sistemi koşulları veya üçüncü taraf sistem bileşenleri bakımından mutlak güvenlik garantisi verilemez.

## 10. Saklama süresi

Optix'in kendi sunucularında kullanıcı verisi saklanmaz. Yerel istatistikler ve tercihler, siz sıfırlayana, uygulama verilerini temizleyene veya uygulamayı kaldırana kadar cihazda kalabilir. İstatistik sıfırlama işlemi tercihlerinizi silmez.

## 11. Çocukların gizliliği

Optix çocuklara özel tasarlanmamıştır ve çocuklardan bilerek kişisel bilgi toplamak amacı taşımaz.

## 12. Politika değişiklikleri

Optix'in işlevleri, kullanılan izinler veya veri işleme uygulamaları değişirse bu politika güncellenebilir. Güncel sürüm bu sayfada yayımlanır; güncelleme tarihi ve uygulama sürümü değiştirilir.

## 13. İletişim

Gizlilikle ilgili soru veya talepler: **onenstudioo@gmail.com**

---

Bu metin Optix'in mevcut işlevleri ve uygulama içindeki veri işleme davranışı hakkında bilgi vermek için hazırlanmıştır. Mağaza beyanları ve yayımlanan uygulama sürümü, bu metinle tutarlı tutulmalıdır.
