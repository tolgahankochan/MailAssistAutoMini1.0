# MailAssistAutoMini1.0
Günlük düzenli olarak asistan bilgisi gönderen n8n mail sistemi. 
# Autonomous Daily Strategy & Logistics Bot 🚀

## Proje Özeti
Kullanıcının lokasyon bazlı lojistik verilerini (İftar/Sahur vakitleri) REST API üzerinden çeken, Google Gemini (LLM) ile bu verileri analiz edip günlük strateji/motivasyon içerikleri üreten ve her sabah otonom olarak HTML formatlı e-posta raporu sunan n8n otomasyon sistemi.

## Kullanılan Teknolojiler
* **Otomasyon Motoru:** n8n
* **Yapay Zeka (LLM):** Google Gemini 1.5 Flash
* **Veri Kaynakları:** Aladhan REST API
* **Haberleşme:** Gmail SMTP / API
* **Formatlama:** JSON, HTML/CSS

## Sistem Mimarisi (Veri Akışı)
1. **Schedule Trigger:** Sistem her sabah saat 09:00'da otonom olarak tetiklenir.
2. **HTTP Request:** Trabzon lokasyonu için Diyanet İşleri protokolüyle günlük astronomik veriler çekilir.
3. **AI Processing:** Google Gemini API'ye anlık istek atılır; sistem rastgele motivasyon, IE terminolojisi ve genel kültür verileri üretir.
4. **Data Formatting & Routing:** Gelen JSON verileri parse edilir (`JSON.parse`) ve kognitif yükü azaltacak karanlık tema (Dark Mode) UI/UX prensiplerine uygun bir HTML şablonuna gömülür.
5. **Delivery:** Rapor, kullanıcının e-posta kutusuna iletilir.

## Kurulum
1. `autonomous-strategy-bot.json` dosyasını indirin.
2. n8n panelinizde "Import from File" seçeneği ile projeyi içeri aktarın.
3. Kendi Google Gemini API anahtarınızı ve Gmail bağlantınızı "Credentials" sekmesinden tanımlayın.
4. HTTP Request düğümünden kendi şehrinizi güncelleyin.
