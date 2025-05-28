# yapayzekafinal
# 🎵 Şarkı Sözü Benzerlik Analizi – Yapay Zeka Ödevi 2

Bu proje, Yapay Zeka dersi kapsamında, Word2Vec ve TF-IDF modelleri kullanılarak Türkçe şarkı sözleri arasında metinsel benzerlik analizi yapılmasını amaçlamaktadır.

## 📌 Proje Amacı

- Genius API üzerinden toplanan şarkı sözleri ile 16 Word2Vec ve 2 TF-IDF modeli eğitildi.
- Verilen bir giriş metni ile, her modelin en çok benzeyen 5 şarkıyı bulması sağlandı.
- Cosine similarity ve Jaccard benzerliği ile değerlendirme yapıldı.
- Anlamsal başarı subjektif olarak da puanlandı.

## 🗃️ Kullanılan Veri

- Türkçe şarkı sözleri (~15MB)
- Temizlenmiş ve ön işlenmiş veri setleri:
  - `lemmatized.csv`
  - `stemmed.csv`

## ⚙️ Kullanılan Yöntemler

- **TF-IDF:** `scikit-learn` kütüphanesi ile
- **Word2Vec:** `gensim` kütüphanesi ile, CBOW ve Skip-gram yapıları kullanılarak
- **Benzerlik Ölçümü:**
  - Cosine Similarity
  - Jaccard Benzerliği
- **Değerlendirme:**
  - Anlamsal benzerlik puanlaması (1–5 arası)
  - 18x18 Jaccard matrisi

## 🧪 Model Yapılandırmaları

| Model Türü  | sg (0=CBOW, 1=Skip) | window | vector_size |
|-------------|----------------------|--------|-------------|
| Word2Vec    | 0 / 1                | 2, 5, 10 | 50, 100     |
| TF-IDF      | -                    | -      | -           |

Toplam: 16 Word2Vec + 2 TF-IDF modeli


---


```txt
numpy
pandas
scikit-learn
gensim
matplotlib
seaborn
