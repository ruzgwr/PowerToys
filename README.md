Microsoft PowerToys, güç kullanıcıların Windows deneyimini ayarlamak ve optimize etmek için kullanabilecekleri bir dizi yardımcı program içeren bir yazılım paketidir. Daha fazla bilgi için [PowerToys hakkında genel bakış ve yardımcı programların nasıl kullanılacağı][usingPowerToys-docs-link] veya [Windows geliştirme ortamları](https://learn.microsoft.com/windows/dev-environment/overview) için diğer araçlar ve kaynaklar için [learn.microsoft.com][usingPowerToys-docs-link]'a gidin!

## Microsoft PowerToys Kurulumu ve Kullanımı

### Gereksinimler

- Windows 11 veya Windows 10 sürüm 2004 (kod adı 20H1 / yapı numarası 19041) veya daha yeni bir sürüm.
- Kurulumcunun, en son sürümü yükleyecektir:
   - [Microsoft Edge WebView2 Runtime](https://go.microsoft.com/fwlink/p/?LinkId=2124703) önyükleyici. Bu, en son sürümü yükleyecektir.

### GitHub üzerinden EXE ile [Önerilen]

[Microsoft PowerToys GitHub sürümler sayfasına gidin][github-release-link] ve en altta bulunan "Assets"e tıklayarak yayındaki dosyaları gösterin. Lütfen bilgisayarınızın mimarisine ve yükleme kapsamına uygun PowerToys kurulumunu kullanın. Çoğu için bu "x64" ve "kullanıcı başına" olacaktır.

| Açıklama       | Dosya Adı | sha256 Karma Değeri |
|----------------|----------|--------------------|
| Kullanıcı başına - x64       | [PowerToysUserSetup-0.74.0-x64.exe][ptUserX64] | 1C4ECE9F11488BAFFAE6B76D2B0504FA18BFFEA11EBC38BCC87F5D86AEA87C7C |
| Kullanıcı başına - ARM64     | [PowerToysUserSetup-0.74.0-arm64.exe][ptUserArm64] | 4F3842FAB0839A361A15A06B7720BA8A0FE7F9AF98EA94245C08DEF37678CA4A |
| Makine geniş - x64   | [PowerToysSetup-0.74.0-x64.exe][ptMachineX64] | 648992E8CEA08F3C63C7CCBD554ADDF500ECBC4560187310BC12E6CB9C2F38E3 |
| Makine geniş - ARM64 | [PowerToysSetup-0.74.0-arm64.exe][ptMachineArm64] | 2B6D92F1A0EA688C7EE882050AC9B030C8B3A18765163FB6D67E5E694A4D4FE3 |

Bu, tercih ettiğimiz yöntemdir.

### Microsoft Store üzerinden

[Mikrosoft Mağaza'nın PowerToys sayfasından](https://aka.ms/getPowertoys) kurun. Windows 11 ve Windows 10 için mevcut olan [yeni Microsoft Store](https://blogs.windows.com/windowsExperience/2021/06/24/building-a-new-open-microsoft-store-on-windows-11/) kullanıyor olmalısınız.

### WinGet üzerinden
PowerToys'u [WinGet üzerinden](https://github.com/microsoft/winget-cli#installing-the-client) indirin. WinGet aracılığıyla PowerToys güncellenirse, mevcut PowerToys yükleme kapsamına saygı duyulacaktır. PowerToys'u yüklemek için aşağıdaki komutu komut istemcisinde / PowerShell'den çalıştırın:

#### Kullanıcı kapsamı yükleyici [varsayılan]
```powershell
winget install Microsoft.PowerToys -s winget
```

#### Makine genişliğinde kapsam yükleyici

```powershell
winget install --scope machine Microsoft.PowerToys -s winget
```

### Diğer kurulum yöntemleri

Bu, Chocolatey ve Scoop gibi [topluluk tarafından desteklenen kurulum yöntemleri](./doc/unofficialInstallMethods.md) gibi yöntemlerdir. Eğer bunlar tercih ettiğiniz kurulum çözümleri ise, kurulum talimatlarını orada bulabilirsiniz.

## Üçüncü Taraf Çalıştırma Eklentileri

Topluluk tarafından oluşturulan [üçüncü taraf eklentilerinin](./doc/thirdPartyRunPlugins.md) bir koleksiyonu, PowerToys ile birlikte dağıtılmayan topluluk tarafından oluşturulmuş eklentileri içerir.

## Katkıda Bulunma

Bu proje, tüm türdeki katkıları memnuniyetle karşılar. Kodlama özellikleri / hata düzeltmeleri dışında, diğer yardımcı yollar arasında spec yazma, tasarım, belgeleme ve hata bulma gibi yollar da bulunmaktadır. Windows'tan en iyi şekilde yararlanmanıza yardımcı olacak bir dizi araç oluşturmak için güç kullanıcı topluluğu ile birlikte çalışmaktan mutluluk duyuyoruz.

**Bir özellik üzerinde çalışmaya başlamadan önce katkıda bulunmak istediğiniz bir özellik üzerinde çalışmaya başlamadan önce**, lütfen [Katkıda Bulunanlar Kılavuzu](CONTRIBUTING.md) okuyun. En iyi yaklaşımı belirlemek, özellik geliştirme sürecinde size rehberlik etmek ve rehberlik ve mentorluk sağlamak, gereksiz veya tekrarlanmış çaba olmamasına yardımcı olmak için sizinle çalışmaktan mutluluk duyarız.

Çoğu katkı, katkılarınızı kullanma izni verdiğinizi ve bunu yapma izniniz olduğunu beyan eden [Katkı Lisans Anlaşması (CLA)][oss-CLA] şartı gerektirir.

## Neler Oluyor

### PowerToys Yol Haritası

Odaklandığımız özellikler ve araçlar listesi olan [öncelikli yol haritamızı][roadmap] burada bulabilirsiniz.

### 0.74 - Eylül 2023 Güncellemesi

Bu sürümde, kararlılık ve iyileştirmelere odaklandık.

**Öne Çıkanlar**

- Windows App SDK 1.4.1'e yükseltildi, WinUI3 araçlarının kararlılığı artırıldı. Yükseltmeye başlayan için teşekkürler [@dongle-the-gadget](https://github.com/dongle-the-gadget)!
- Metin Çıkarıcı, yeni bir üst örtü ve tablo modu ile birlikte 2.0 sürümüne yükseltildi, ve kullanıcı deneyimini iyileştiren diğer geliştirmeler yapıldı. Teşekkürler [@TheJoeFin](https://github.com/TheJoeFin)!
- FancyZones kararlılığı iyileştirildi, bazı düzen sıfırlamalarını düzeltildi ve Windows 11'de yeni oluşturulan pencerelerin işlenmesi geliştirildi.
- Watson ve kullanıcının etkinlik kaydediciye raporladığı sessiz çökme hataları düzeltildi.

### Genel

- Pencereler Ayarlarında animasyonları kapatmak artık PowerToys'te de animasyonları kapatır.
- Windows App SDK bağımlılığı 1.4.1'e yükseltildi. Yükseltmeye başlayan için teşekkürler [@dongle-the-gadget](https://github.com/dongle-the-gadget)!
- Yönetici olarak çalıştırıldığında minik etiket ve uygulama başlıkları gösterilir. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!
- Win UI Topluluk Araç Seti bağımlılığı 8.0'a yükseltildi. Teşekkürler [@niels9001](https://github.com/niels9001)!

### Awake

- Uygulamanın simgesine küçültülmüş varyantlar eklendi. Teşekkürler [@morriscurtis](https://github.com/morriscurtis)!

### Renk Seçici

- Düzenleyiciye yeni bir renk eklendikten sonra, geçmiş yeni rengi görüne kaydıracak. Teşekkürler [@peerpalo](https://github.com/peerpalo)!

### Kırp ve Kilitle

- Bir pencereyi yeniden ataşlemeye çalışırken oluşan Kırp ve Kilitle çökmesi düzeltildi. Bunun yerine bir hata mesajı gösterilir.

### FancyZones

- Süreci ve ana iş parçasının önceliğini normal olarak ayarlayın.
- Windows 11'de yeni oluşturulan pencerelerin işlenmesi düzeltildi.
- FancyZones Düzenleyicisi'ni açarak düzenleri sıfırlayan senaryolar düzeltildi.

### Dosya Gezgini Eklentileri

- SVG küçük resimler oluştururken CPU kullanımı optimize edildi.
- Gcode küçük resimlerinin işlenmesi iyileştirildi, JPG ve QOI formatlarını da içerir. Teşekkürler [@pedrolamas](https://github.com/pedrolamas)!
- Telemetri gönderirken oluşan hatalar daha iyi ele alındı, rapor edilen çökmeleri düzeltiyordu.
- Optimizasyon öncesi gibi merkezlenmemiş bazı küçük resimler düzeltildi.

### Dosya Kilidi

- PID'si 65535'ten büyük olan işlemler tarafından açılan dosyaları gösterir. Teşekkürler [@poke30744](https://github.com/poke30744)!
- Keşfediciyi çökertmeye neden olan bir GDI nesne sızıntısı düzeltildi.

### Faremi Bul

- Sıcak tuş dahil olmak üzere yeni etkinleştirme yöntemleri eklendi. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!

### Hosts Dosyası Düzenleyici

- Hosts dosyasındaki varsayılan ACME örnek girdilerini görmezden gelin. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!
- Kaydetme hata işleme iyileştirildi ve daha iyi hata mesajları eklendi. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!
- Yönetici olarak başlatma işlemini sinyal verirken bir hata kontrolü düzeltildi.
- Bağlam menüsü yeniden düzenlendi. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!
- Windows App SDK 1.4'e yükseltme sonrasında başlık çubuğunda örtüşen iletiler düzeltildi. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!

### Klavye Yöneticisi

- Düz eksi tuşu ile sayı takımı eksi tuşu arasında ayrım yapın.

### Sınırlar Arası Fare

- Uygulamayı yeniden başlatmaya çalışırken oluşan çökme düzeltildi.

### Peek

- HTML dosyalarında Peek kullanmak varsayılan olarak bir tarayıcının varsayılan davranışına benzer şekilde beyaz bir arka plan gösterir.
- Dark temasında dosya değiştiğinde beyaz flaş düzeltildi

## PowerRename

 - Yeni sıralama yöntemindeki büyük sayıcı değerlerinden kaynaklanan çökertilen hatayı düzeltildi.

## PowerToys Run

 - Artık Kabuk eklentisi tarafından kullanılan kabuğu seçmek mümkün.
 - Eklenti seçeneklerine combobox seçenek türü eklendi.
 - Calculator eklentisinde ondalık sayılarının ondalık işareti (`.`) karakterinin ondalık ayırıcı veya basamak ayırıcı olarak kullanılmadığı yerel ayarlarda yanlış yorumlanmasına neden olan bir hata düzeltildi.
 - Program eklentisinin bir programın küçük resmini başlatıldığında yüklemekte başarısız olduğunda kararlılığı iyileştirildi.
 - Bazı eklentilerin sorgulanması için Pinyin kullanımı Artık Ayarlar'da açılabilir. Teşekkürler [@ChaseKnowlden](https://github.com/ChaseKnowlden)!
 - Eklenti için seçenek türlerini yeniden düzenlendi ve gelecekte kullanılmak üzere sayı, dize ve bileşik türler eklendi. Teşekkürler [@htcfreek](https://github.com/htcfreek)!
 - Ayarlar eklentisinde Windows güncellemelerini arama girişi düzeltildi. Teşekkürler [@htcfreek](https://github.com/htcfreek)!

## Quick Accent

 - "Tüm diller" karakter kümesi şimdi her mevcut dil için karakterleri programatik olarak sorgulayarak hesaplanır. Teşekkürler [@dannysummerlin](https://github.com/dannysummerlin)!
 - Norwegian ve Swedish dillerine é eklendi. Teşekkürler [@Aaron-Junker](https://github.com/Aaron-Junker)!
 - "Tüm diller" karakter kümesine yalnızca bir kez hesaplamak üzere çalışma zamanı önbelleği eklendi.

## Registry Preview

 - Başlangıçta odaklanma sorunları düzeltildi.
 - Verileri Windows Kayıt Düzenleyici'ye benzer bir şekilde göstermek için veri görselleştirmesi iyileştirildi. Teşekkürler [@dillydylann](https://github.com/dillydylann)!

## Runner

 - Uyarı penceresinden hata raporu oluşturulduğunda askıda kalma düzeltildi. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!

## Settings

 - OOBE penceresinin Windows teması değişikliklerine nasıl tepki verdiği iyileştirildi.
 - FancyZones için "Geçerli bölgede pencere arasında geçiş yap" "Sonraki pencere" kısayolunu değiştirmeyi imkansız kılan bir sorun düzeltildi.
 - Renk Seçici sayfasında bir renk için yinelenen bir isim girildiğinde çökme düzeltildi ve renk düzenlemeyi iptal etme iyileştirmesi yapıldı. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!

## Text Extractor

 - Yeni bir üst örtü, tablo modu ve daha fazla Kullanıcı Dostu geliştirmeler ile Text Extractor 2.0. Teşekkürler [@TheJoeFin](https://github.com/TheJoeFin)!

## Documentation

 - SECURITY.md 0.0.2'den 0.0.9'a güncellendi. Teşekkürler [@Aaron-Junker](https://github.com/Aaron-Junker)!
 - README ve ana geliştirme belgesi netlik ve eksiksizlik açısından iyileştirildi. Teşekkürler [@codeofdusk](https://github.com/codeofdusk) ve [@aprilbbrockhoeft](https://github.com/aprilbbrockhoeft)!

## Development

 - Belirli yerel ayarlara bağlı olarak başarısız olan PowerToys Run DateTime eklenti testleri düzeltilerek, tüm geliştirici makinelerinde doğru şekilde çalıştırılabilmeleri sağlandı.
 - Belirli ağ arabirimleri için başarısız olan PowerToys Run System eklenti testleri düzeltilerek, tüm geliştirici makinelerinde doğru şekilde çalıştırılabilmeleri sağlandı. Teşekkürler [@snickler](https://github.com/snickler)!
 - GitHub /helped komutundaki bir markdown hatası düzeltildi.
 - Yeni Visual Studio'da oluşturulan .cs dosyaları otomatik olarak başlık eklenir. Teşekkürler [@davidegiacometti](https://github.com/davidegiacometti)!

#### 0.75 Sürümü için Planlananlar

 [v0.75][github-next-release-work] sürümü için aşağıdaki öğeler üzerinde çalışacağız:

 - Dil seçimi
 - .NET 8 yükseltmesi
 - PowerToys Run eklentilerini yönetmek için Politika desteği.
*Dikkat*: 0.75 sürümü için bir kırılma değişikliği planlanmıştır, her eklentinin GPO aracılığıyla kontrol edilebilmesi için eklentinin kimlik belirtmesi gerekecektir. Üçüncü taraf eklenti geliştiricileri için daha fazla ayrıntı için https://github.com/microsoft/PowerToys/pull/27468 adresini kontrol edin.

 - Yeni araç: Ortam Değişkenleri Düzenleyici. İşte çalışma aşamasında bir önizleme:

![Ortam Değişkenleri Düzenleyici WIP](https://github.com/microsoft/PowerToys/assets/26118718/f99532a8-5aae-481b-a662-19a95f4aa03d)

 - Yeni Ayarlar ana sayfa

Tabii ki, işte tam metnin Türkçe çevirisi:

---

## PowerToys Topluluğu

PowerToys ekibi, muhteşem ve aktif bir topluluk desteği [support of an amazing active community][community-link]ne sahip olduğu için son derece minnettardır. Yaptığınız çalışmalar son derece önemlidir. Hataların bildirilmesi, belgelerin güncellenmesi, tasarım rehberliği veya özelliklerin yazılmasında yardımınız olmadan PowerToys bugünkü haline gelemezdi. Size teşekkür etmek ve çalışmalarınızı tanımak istiyoruz. Aydan aya, PowerToys'u doğrudan daha iyi bir yazılım haline getirmemiz için yardımcı oluyorsunuz.

## Davranış Kuralları

Bu proje [Microsoft Açık Kaynak Davranış Kuralları'nı][oss-conduct-code] benimsemiştir.

## Gizlilik Bildirimi

Uygulama temel telemetriyi kaydeder. Telemetri Verilerimiz sayfası (Yakında) telemetri trendlerini içermektedir. Daha fazla bilgi için lütfen [Microsoft gizlilik bildirisini][privacy-link] okuyun.

[oss-CLA]: https://cla.opensource.microsoft.com
[oss-conduct-code]: CODE_OF_CONDUCT.md
[community-link]: COMMUNITY.md
[github-release-link]: https://aka.ms/installPowerToys
[microsoft-store-link]: https://aka.ms/getPowertoys
[winget-link]: https://github.com/microsoft/winget-cli#installing-the-client
[roadmap]: https://github.com/microsoft/PowerToys/wiki/Roadmap
[privacy-link]: http://go.microsoft.com/fwlink/?LinkId=521839
[vidConfOverview]: https://aka.ms/PowerToysOverview_VideoConference
[loc-bug]: https://github.com/microsoft/PowerToys/issues/new?assignees=&labels=&template=translation_issue.md&title=
[usingPowerToys-docs-link]: https://aka.ms/powertoys-docs
