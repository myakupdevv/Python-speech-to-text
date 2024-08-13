## Script Genel Bakış

Bu script, bir ses dosyasındaki konuşmayı metne dönüştürmek için OpenAI API'sini kullanır. Ses dosyasını parçalara ayırır, bu parçaları OpenAI'ye gönderir, metinleri birleştirir ve isteğe bağlı olarak özetler ve zaman damgaları oluşturur. Desteklenen dosya türleri arasında `mp3`, `mp4`, `mpeg`, `mpga`, `m4a`, `wav` ve `webm` bulunmaktadır.

### Adım 1: Python ve Kütüphaneleri Yükleyin

1. **Python Yükleyin**:
   - **macOS**: Terminal'i açın ve şunu çalıştırın:
     ```sh
     brew install python
     ```
   - **Windows**: [Python web sitesinden](https://www.python.org/downloads/windows/) indirin ve yükleyin, "Add Python to PATH" seçeneğini işaretleyin.

2. **Kütüphaneleri Yükleyin**:
   ```sh
   pip install pydub openai
   ```

### Adım 2: OpenAI API Anahtarını Alın

1. [OpenAI](https://platform.openai.com) adresinde kaydolun ve giriş yapın.
2. Kontrol panelinizde yeni bir API anahtarı oluşturun.

### Adım 3: API Anahtarını Ayarlayın

**macOS:**
1. Terminal'i açın.
2. Shell profilinizi düzenleyin:
   ```sh
   nano ~/.bash_profile
   ```
3. Aşağıdakileri ekleyin:
   ```sh
   export OPENAI_API_KEY='your_openai_api_key'
   ```
4. Değişiklikleri kaydedin ve uygulayın:
   ```sh
   source ~/.bash_profile
   ```

**Windows:**
1. Komut İstemi'ni açın.
2. Şunu çalıştırın:
   ```cmd
   setx OPENAI_API_KEY "your_openai_api_key"
   ```
3. Komut İstemi'ni yeniden başlatın.

### Adım 4: Script'i Çalıştırın

1. Script'i `transcribe.py` olarak kaydedin.
2. Komut İstemi veya Terminal'i açın, script dizinine gidin.
3. Şunu çalıştırın:
   ```sh
   python transcribe.py path_to_your_audio_file
   ```
   Python 3 için:
   ```sh
   python3 transcribe.py path_to_your_audio_file
   ```

Örnek:
```sh
python transcribe.py audio.m4a
```

### İsteğe Bağlı Parametreler

- `--sum`: Özet oluştur.
- `--time`: Zaman damgalarını dahil et.

Örnek:
```sh
python transcribe.py audio.m4a --sum --time
```
