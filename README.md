# Valmeryn2 Client Source

Valmeryn2 istemcisinin C++ kaynak kodu ve Windows build yapılandırması.

## Gereksinimler

- Windows 10/11
- CMake
- Visual Studio C++ iş yükü ve Windows SDK
- Depoda sağlanan/vendor bağımlılıkları

## Derleme

PowerShell veya Developer Command Prompt içinde:

```powershell
cmake -S . -B build
cmake --build build --config Release
```

Build araç seti veya SDK seçiminiz farklıysa CMake'e uygun Visual Studio generator/architecture belirtin. Derlenen executable'ı yalnızca aynı kaynak revizyonuna ait client assets ile kullanın.

## Proje düzeni

- `src/`: istemci C++ kaynakları
- `extern/`, `vendor/`: bağımlılıklar
- `buildtool/`: build yardımcıları

## Entegrasyon kuralı

Sunucu ve istemci packet tanımları birlikte değişir. Paket başlığı, uzunluğu veya yeni UI/network akışı eklenirken karşı uçtaki eşleşme ve packet-size kayıtları da aynı değişiklikte ele alınmalıdır. Çalışır oyun istemcisi doğrulanmadan bir sistemi hazır saymayın.

Sistem planı ve önceki çalışma notları çalışma alanındaki `YENI_PROJE_DEVIR_RAPORU.md` dosyasındadır.
