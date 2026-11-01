# orion-ai-assistant.github.io

Orion'un telefon eşleştirme bağlantıları: `https://orion-ai-assistant.github.io/p#<eşleştirme>`.

- `p.html`: Bağlantıyı Orion uygulamasına verir. `#` sonrası tarayıcıdan hiçbir sunucuya gitmez, sayfa onu okuyup adres çubuğundan siler. Dışarıdan dosya, çerez, takip yok; Content-Security-Policy yalnızca kendi betiğine izin verir.
- `.well-known/assetlinks.json`: Android App Links. Uygulama (`com.lonelyfrog.orionai`) yüklüyse bağlantı tarayıcıya hiç uğramadan uygulamada açılır.
  - Listede uygulamayı imzalayan sertifikaların SHA-256'sı olmalı. Şu an geliştirme PC'sinin debug anahtarı var.
  - Google Play'e çıkınca Play Console > Uygulama bütünlüğü > Uygulama imzalama sayfasındaki SHA-256 da eklenir.
- `.nojekyll`: `.well-known` klasörünün yayınlanması için.

Eşleştirme biçimi Hub'da `services/hub/src/orion/api/mobile_security.py` içinde: `pairing_token`.
