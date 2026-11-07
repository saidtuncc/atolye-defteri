# Canlıdan dersler

[← Ana sayfa](../README.md)

Gerçek işletmelerin her gün kullandığı bir sistemde yaşanan olaylardan çıkan kurallar. Her biri en az bir kez canlıda yaşandı.

---

### 1. Sağlıklıyken sessiz olması, alarmın çalıştığını kanıtlamaz
Bildirim sistemine "ilettim" kaydı eklenene kadar bir dizi kritik olayın hiç iletilmediği fark edilmemişti. Artık her bildirimin iletilip iletilmediği kaydediliyor ve alarm zinciri sahte bir arızayla düzenli olarak sınanıyor.

### 2. Prova edilmemiş yedek, yedek değildir
Geri yükleme tarifleri birbiriyle çelişen birkaç belgede duruyordu ve hiçbiri denenmemişti. Tek bir geri yükleme aracı yazıldı ve tatbikat yapıldı: kurulum yedekten yaklaşık 2 saniyede ayağa kalktı.

### 3. "Yedeklenecek bir şey yok" ile "hiç bakmadım"ı ayır
Bir yedek aracı, desteklemediği bir veri yerleşiminde boş liste bulup "başarılı" diye çıkıyordu. Her gün yeşil yanıyor ama hiçbir şey yedeklemiyordu. Bu yedeksiz kalmaktan kötüdür, çünkü yedeğin var sanırsın. Artık her arşiv açılıp içeriği doğrulanıyor.

### 4. Para, yayının tek kırmızı çizgisidir
Her yayından önce ve sonra bütün işletmelerin para toplamları sayılır ve iki sayı birebir aynı olmalıdır. Yolda iki tuzak çıktı: "ödendi" sütununu toplamak para değil ödenmiş iş *sayısını* verir, tahsilat ise kuruş cinsinden tutulur.

### 5. Yerelde yeşil, canlıda yeşil demek değildir
Yerelde bütün testler geçerken kanarya halkasında birkaç test kırıldı. Sorun üründe değil testteydi: test, sunucuda bulunmayan bir kütüphaneye dayanıyordu. Kanarya kırmızıysa ilk soru şu olmalı: *ürün mü bozuk, sınav mı?*

### 6. "Yayın tamam" kararı dışarıdan verilir
Dosyalar doğru, süreçler yeniden başlamış görünürken birkaç gün boyunca eski kod servis edildi. Artık yayın, sürüm bilgisi bütün adreslerden dışarıdan okunup doğrulanmadan tamamlanmış sayılmıyor.

### 7. Önce bekçiyi durdur
Bir taşıma sırasında bütün süreçler durduruldu ve kontroller yeşil verdi. Ama zamanlanmış bir bekçi görevi birkaç dakika sonra eski süreçleri yeniden başlattı ve trafik iki makine arasında bölündü. Dışarıdan bakınca iki taraf da "çalışıyor" görünüyordu.

### 8. Bekçinin sırası önemlidir
Eski bir bekçi, süreç kapalıyken gelen hatayı "bağlantı koptu" diye yorumlayıp bağlantıyı yeniden kuruyor ve yeni bir adres üretiyordu. Müşterilere gönderilmiş bütün takip bağlantıları ölüyordu. Doğru sıra: önce süreç, sonra bağlantı.

### 9. Küçük bir eleme kuralı iki gün yedeksiz bıraktı
Paketleme sırasında bir klasörü elemek için yazılan desen, aynı adı taşıyan başka bir klasörü de eledi. Yedek aracı sunucuya hiç gitmedi ve kimse fark etmedi, çünkü aracı bulamayan nöbetçi sessizce çıkıyordu. Artık paket kendi içeriğini denetliyor; kritik bir dosya eksikse paket hiç üretilmiyor.

### 10. Deneme verisini canlı deftere yazma
Yeni bir özelliği denemek için canlı ayarlar değiştirildi ve kullanıcı tam o anda yarım bir sayfa gördü. Kod doğruydu; sayfayı bozan deneme verisiydi. Denemeler yalıtılmış bir defterde yapılır.

### 11. Ölçüm yetmez, ekrana bak
Bir arayüz animasyonu canlıda yazıyı ters gösteriyordu. Testler de ölçümler de bunu yakalayamadı; yalnız ekran görüntüsü gösterdi. Her arayüz değişikliği gerçek ekranda kontrol edilir.

---

> Her bileşen, olmadığı gün neyin kaybedildiğini anlatan bir notla birlikte yazılır. Kod yeniden yazılabilir; ama bir kaza tekrarlanmasın diye yazılmış bir cümle yeniden keşfedilemez.
