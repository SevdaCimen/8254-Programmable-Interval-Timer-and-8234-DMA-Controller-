# 8254 Programmable Interval Timer and 8234 DMA Controller 


8254  Programmable Interval Timer

![825](https://user-images.githubusercontent.com/26030084/34914660-bbca718a-f927-11e7-896e-fccd435966ca.png)


Intel 8253 ve 8254, zamanlama ve sayma işlevlerini yerine getiren Programlanabilir Aralık Zamanlayıcıları
(Programmable Interval Timers) 'dir. Tüm x86 bilgisayarlarında bulunurlar.8254 programlanabilir zaman aralığı / sayaç
mega işlevi, mikrobilgisayar sistemi tasarımında ortak zamanlama kontrol problemlerini çözmek için tasarlanmış
yüksek performanslı bir işlevdir. Üç bağımsız 16 bit sayaç sağlar ve her sayaç farklı bir modda çalışabilir.Tüm modlar
yazılımla programlanabilir.
8254 mega işlevi, herhangi bir mikrobilgisayar sistemindeki en yaygın sorunlardan biri olan yazılım kontrolü altındaki
doğru zaman gecikmelerinin üretilmesi problemini çözer.Yazılımda zamanlama döngüleri kurmak yerine 8254 mega
işlevi, istenen gecikme için sayaçlardan birini programlayarak ihtiyaçları karşılamak üzere programlanabilir.Zamanlayıcı,
kanallar adı verilen üç sayaç içerir.Her kanal, altı moddan birinde çalışacak şekilde programlanabilir.
Programlandıktan sonra kanallar görevlerini bağımsız olarak yerine getirebilir. Zamanlayıcı, yerine getirdiği kritik işlev
ve çoğu aygıt bağlı olduğu için genellikle IRQ-0'a (en yüksek öncelikli donanım kesmesi) atanır [2].
Ana temelde Intel 8254, mikrobilgisayar sistem tasarımında ortak zamanlama kontrol problemlerini  çözmek için
tasarlanmış bir zaman sayıcı / sayaç aygıtıdır. 8254, 8253'ün yüksek hızlı sürümüdür.




8234 DMA Controller 

![dma](https://user-images.githubusercontent.com/26030084/34914672-0def2334-f928-11e7-944f-6048513ec519.png)

DMA denetleyicisinin uygun kanalı, bellek başlangıç adresi ve aktarım sayımı ile programlandıktan sonra, ilgili periferik
veri okuma veya yazmaya başlamak üzere ayarlanır.
Örneğin, ses örnekleri istemek için bir sektöre veya ses kartına okumak üzere bir disk denetleyicisine bir komut
gönderilebilir. Aşağıdaki sıra kademeleri, döngü çalma modunda bir DMA aktarımı için gerçekleşir:


1. Periferik her bayt aktarabildiğinde DMA talep hattını DMA Controller’a atar.
2. DMA denetleyicisi CPU'nun bekletme isteği pimini belirtir.
3. CPU kontrol devresi yürütmeyi askıya alabildiğinde (bir talimatın sonunda veya T3'te bekleme durumları
ekleyerek), DMA denetleyicisine bekletme onayı (HOLDA) sinyali verir ve adres, veri ve kontrol veri yolu
sinyallerini yüzer.
4. DMA denetleyicisi daha sonra bellek adresini adres veri yoluna koyar, denetime MEMR * artı IOW * veya MEMW *
artı IOR * işaret eder.
5. Veriyoluna iletir ve uygun DMA onay hattını çevre birimine bildirir.
6. Periferik, veriyi veri yoluna okur veya yazarak DMA onaylama sinyaline tepki verir.
7. Aynı zamanda hafıza MEMR * / MEMW * kontrol sinyaline yanıt verir ve bu da verilerin doğrudan bellekten /
hafızadan okunmasına / yazılmasına neden olur.
8. Veri yolu çevriminin sonunda DMA denetleyicisi bekletme isteği satırını geçersiz kılar ve CPU bir sonraki DMA
isteğine kadar devam ettirmeye devam edebilir [
