# Projecte

Bu uygulama, C# ve SQL kullanılarak geliştirilmiş bir proje yönetim sistemidir. Kullanıcıların projeleri, görevleri ve çalışanları etkili bir şekilde yönetmelerine olanak tanır. Uygulama, ilerlemeyi ve son teslim tarihlerini izlemeye odaklanır.

## Özellikler

### Proje Yönetimi
- Kullanıcılar, sistemde birden fazla proje tanımlayabilir.
- Her proje, bir başlangıç tarihi ve bitiş tarihi içerir.
- Kullanıcılar, giriş yaptıktan sonra tüm projelerin bir listesini görebilir.
- Proje yoksa, kullanıcılar yeni bir proje ekleyebilir.
- Kullanıcılar, projelere görevler ekleyebilir ve görevler için başlangıç ve bitiş tarihlerini belirleyebilir.

### Görev Yönetimi
- Görevler projelere eklenebilir ve belirli çalışanlara atanabilir.
- Her görev şunları içerir:
  - Başlangıç tarihi
  - Tahmini efor (adam-gün olarak)
  - Bitiş tarihi
- Görevler üç duruma sahip olabilir:
  - **Tamamlanacak**
  - **Devam Ediyor**
  - **Tamamlandı**
- Zamanında tamamlanan görevlerin durumu otomatik olarak "Tamamlandı" olarak güncellenir.
- Görevler gecikirse, projenin bitiş tarihi buna göre güncellenir ve gecikme süresi kullanıcı arayüzünde gösterilir.

### Çalışan Yönetimi
- Kullanıcılar, sisteme çalışan ekleyebilir, güncelleyebilir veya silebilir.
- Çalışanlar, özel bir bölümde listelenir.
- Bir çalışana tıklandığında, detay sayfasında şu bilgiler gösterilir:
  - Çalışanın atanmış olduğu projeler ve görevler.
  - "Tamamlandı," "Devam Ediyor," veya "Başlayacak" olarak kategorize edilmiş görevler.
  - Çalışanın zamanında tamamladığı ve tamamlayamadığı görevlerin istatistikleri.

## Gereksinimler

### Ön Koşullar
- **C# Geliştirme Ortamı**: Uygulamanın çalışması için uyumlu bir C# sürümünün yüklü olması gerekir.
- **SQL Veritabanı**: Sistemin verileri depolamak için yerel bir SQL veritabanı kullanır. Gerekli tablolar ve veritabanı yerelde oluşturulmalıdır.

### Veritabanı Kurulumu
- Uygulamayı çalıştırmadan önce SQL veritabanında gerekli tabloları oluşturun.
- `App.config` dosyasındaki veritabanı bağlantı dizesinin yerel ayarlarınızla eşleştiğinden emin olun.

## Kurulum ve Kullanım

1. Bu depoyu klonlayın:
   ```bash
   git clone <repository-url>
   ```

2. `Projecte.sln` çözüm dosyasını C# geliştirme ortamınızda (ör. Visual Studio) açın.

3. SQL veritabanı bağlantısını yapılandırın:
   - `App.config` dosyasındaki bağlantı dizesini düzenleyerek yerel veritabanınızı işaret edin.
   - Sağlanan veritabanı şemasını içe aktarın ve gerekli tabloları doldurun.

4. Uygulamayı derleyin ve çalıştırın.

5. Proje yönetim panosuna erişmek için giriş yapın.

## Nasıl Çalışır

- **Pano**: Projelerin bir listesini görüntüler. Proje yoksa yeni bir proje eklenebilir.
- **Proje Detayları**: Bir projeye tıklayarak görevlerini görüntüleyebilir veya ekleyebilirsiniz.
- **Görev Atama**: Görevleri çalışanlara atayın ve ilerlemelerini takip edin.
- **Çalışan Detayları**: Bir çalışana ait detaylı bilgileri görüntüleyin, atanmış görevlerini ve performans istatistiklerini inceleyin.

## Gelecek Geliştirmeler
- Harici görev yönetim araçlarıyla entegrasyon.
- Görev güncellemeleri ve son tarihler için e-posta bildirimleri.
- Proje performansı için detaylı raporlama ve analiz.

## Lisans
Bu proje, eğitim amaçlı olarak tasarlanmıştır ve ticari kullanım için lisanslanmamıştır.

