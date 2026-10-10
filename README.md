# biProxy dağıtımları

macOS için biProxy kurulum paketleri ve imzalı güncelleme manifesti.

İlk sürüm: **1.0.0-beta01**. Sonraki beta sürümleri `1.0.0-beta02`, `1.0.0-beta03` şeklinde ilerler. Kararlı sürüm `1.0.0` aynı sürümün tüm betalarından daha yenidir.

[İndirilecek sürümler](https://github.com/ahmet-ozberk/biProxy-version/releases)

- `biProxy-<sürüm>-macos-arm64.dmg`: Apple Silicon Mac için ilk kurulum.
- `biProxy-<sürüm>-macos-arm64.zip`: uygulama içi güncelleme paketi.
- Intel paketleri yayımlandığında `macos-x64` adıyla ayrıca listelenir.
- `update.json`: Ed25519 imzalı manifest. Uygulama her açılışta bu dosyayı kontrol eder.

Manifest adresi: `https://raw.githubusercontent.com/ahmet-ozberk/biProxy-version/main/update.json`

Beta yayınları GitHub'da **Pre-release** olarak işaretlenir. Bu nedenle manifest `releases/latest` yerine yukarıdaki sabit adreste tutulur. Manifest yalnızca ilgili paketler yüklendikten sonra güncellenir.

## Kurulum

DMG'yi açıp biProxy uygulamasını Applications klasörüne taşı. Uygulama içinden Ayarlar → Genel → Güncellemeleri kontrol et yoluyla yeni sürümü indir; Yeniden başlat ve kur ile kurulumu tamamla.

Mevcut paketler ad hoc imzalıdır; Developer ID imzası ve notarization henüz uygulanmamıştır. İlk açılışta macOS ek onay isteyebilir.

## Güncelleme imzası

Public key (Ed25519, X.509 DER / Base64):

```text
MCowBQYDK2VwAyEA3HJh4Lez2tXfqz/HHF+jXhEUPUsq114kLES74qQhwrc=
```

Özel imza anahtarı bu depoda tutulmaz. Paket bütünlüğü SHA-256 ile ve manifestin yayıncıya ait olduğu Ed25519 imzasıyla doğrulanır.
