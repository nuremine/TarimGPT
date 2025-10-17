# 🌾 TarımGPT: Çiftçinin Dijital Asistanı  

### 👩‍💻 Geliştirici: Emine Nur Aba  
Bu proje, **Akbank Generative AI Bootcamp** kapsamında geliştirilmiştir.  
Amaç, çiftçilerin tarım, bitki bakımı ve ziraat konularında yapay zeka destekli öneriler almasını sağlamaktır.  

---

## 🚜 Proje Amacı  
TarımGPT, çiftçilerin günlük tarımsal ihtiyaçlarına yanıt veren, RAG (Retrieval-Augmented Generation) temelli bir **tarım asistanı chatbot** olarak tasarlanmıştır.  
Bu sistem, tarımsal verilerden beslenerek çiftçilere tavsiyeler sunar.  

---

## 🌱 Veri Seti Hakkında  
İlk sürümde küçük bir örnek bilgi tabanı (sabit veri) kullanılmaktadır.  
İleri aşamalarda:  
- T.C. Tarım ve Orman Bakanlığı açık verileri  
- FAO (Birleşmiş Milletler Gıda ve Tarım Örgütü) tarım raporları  
- Çiftçi sorularından oluşturulan dinamik veri setleri  
kullanılacaktır.  

---

## 🧠 Kullanılan Teknolojiler  
- **Python** 🐍  
- **Streamlit** (web arayüzü)  
- **LangChain** (RAG mimarisi)  
- **FAISS** (vektör veritabanı)  
- **Sentence Transformers** (embedding modeli)  
- **Flask** (API bağlantısı)  
- **dotenv** (anahtar yönetimi)

---

## ⚙️ Kurulum (Çalıştırma Adımları)

### 1️⃣ Gerekli paketleri yükle:
```bash
pip install -r requirements.txt

