# Oltalama (Phishing) Sitesi Tespiti

Veri madenciliği dersi projesi. URL'lerden çıkarılan özelliklerle oltalama (phishing) sitelerini tespit ediyoruz.

## Amaç
- URL'lerden özellik çıkarmak: uzunluk, `@` işareti, nokta sayısı, IP adresi kullanımı, HTTPS vb.
- **Karar Ağacı**, **Random Forest** ve **XGBoost** modellerini karşılaştırmak
- Karar ağacından okunabilir "EĞER ... İSE sahte" kuralları çıkarmak
- "URL yapıştır, sonucu gör" arayüzü (Streamlit)

## Veri seti
[PhiUSIIL Phishing URL Dataset](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset) (UCI, 2024): yaklaşık 235 bin URL.
Veri dosyaları repoya eklenmez; `data/` klasörüne indirilir.

## Klasör yapısı
```
data/        veri dosyaları (git'e eklenmez)
notebooks/   keşifsel analiz ve model deneyleri
src/         özellik çıkarma ve eğitim kodu
app/         Streamlit arayüzü
```

## Kurulum
```bash
git clone <repo-adresi>
cd phishing-tespiti
pip install -r requirements.txt
```

## Plan
- [ ] Veriyi indirme ve keşifsel analiz (EDA)
- [ ] URL'den özellik çıkarma (`src/features.py`)
- [ ] Model eğitimi ve karşılaştırma (Accuracy, Precision, Recall, F1, ROC-AUC)
- [ ] Karar ağacından kural çıkarma
- [ ] Streamlit arayüzü
- [ ] Rapor ve sunum
