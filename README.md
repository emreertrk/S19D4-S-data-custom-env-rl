## 🧱 Özel Ortam

Bu görevde, **ızgara tabanlı navigasyon ortamının** birebir aynısını tasarlayıp uygulayacaksınız.

- Ajan ızgaranın bir köşesinde başlar.
- Amaç karşı köşeye ulaşmaktır.
- Izgarada ajanın kaçınması gereken engeller veya "delikler" bulunabilir.

🚧 Başlamadan önce: İlk görevde açıklandığı gibi gerekli paketleri kurduğunuzdan emin olun

## Çalışma Notları

Bu proje, Gymnasium'un `Env` yapısıyla 3×3'lük özel bir ızgara navigasyon ortamı (`CustomGridEnv`) yazar ve Stable Baselines3 DQN ajanını bu ortamda eğitir. Şablon yönerge notebook'u yerine kendi notebook'um (`GridEnv-DQN.ipynb`) kullanıldı.

1. Ortam: Workintech'in `S19D41.0-S-reinforcement-env` deposundaki `requirements.txt` ile kurulan `reinforcement-env` sanal ortamı (Python 3.12.9). Proje klasöründe `pyenv local reinforcement-env` ile etkinleştirilir.
2. `jupyter notebook` ile notebook'u aç ve hücreleri sırayla çalıştır. DQN eğitimi CPU'da yaklaşık 21 saniye sürer.
3. Eğitilen model `models/` klasörüne yazılır. `.zip` dosyaları `.gitignore` içindedir, repoda yoktur, notebook çalıştırılınca yeniden oluşur.

Özet: Ortam 3×3, başlangıç (0,0), hedef (2,2), delik (2,1). Hedef +10, delik -10, adım başına -0.1 ödül verir. Eğitimsiz model -5.00, eğitilen DQN 9.70 (en iyi mümkün skor) aldı. Ayrıntılar ve sınırlılıklar notebook'un sonuç bölümünde.
