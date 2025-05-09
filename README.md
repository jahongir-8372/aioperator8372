# aioperator8372
suniy entilecktga asoslangan call operatori - tez tibbiy yordam uchun 
# Tez Tibbiy Yordam Operatori - O'rnatish qo'llanmasi

Bu qo'llanma sizga Python-based Tez Tibbiy Yordam Operatorini o'rnatish va ishga tushirishni ko'rsatadi.

## Talablar

- Python 3.9 yoki yuqoriroq versiya
- pip (Python paket menedjeri)
- OpenAI API kalit
- Muxlisa AI API kalit

## O'rnatish qadamlari

1. Repozitoriyani klonlash yoki fayllarni yuklab olish

```bash
git clone https://github.com/username/tibbiy-yordam-operatori.git
cd tibbiy-yordam-operatori
```

2. Virtual muhit yaratish va faollashtirish

```bash
python -m venv venv
# Linux/Mac
source venv/bin/activate
# Windows
venv\Scripts\activate
```

3. Kerakli paketlarni o'rnatish

```bash
pip install -r requirements.txt
```

4. `.env` faylini sozlash

`.env.example` faylini `.env` ga nusxalang va o'z API kalitlaringizni kiriting:

```bash
cp .env.example .env
# Keyin .env faylini tahrirlang
```

5. Ilovani ishga tushirish

```bash
uvicorn app:app --reload
```

6. Ilova http://localhost:8000 manzilida ishlaydi

API hujjatlarini http://localhost:8000/docs sahifasida ko'rishingiz mumkin.

## Docker bilan ishga tushirish

Docker o'rnatilgan bo'lsa, quyidagi buyruqlar orqali ilovani konteyner sifatida ishga tushirishingiz mumkin:

```bash
# Docker image yaratish
docker build -t tibbiy-yordam-operatori .

# Konteyner ishga tushirish
docker run -p 8000:8000 --env-file .env tibbiy-yordam-operatori
```

## API endpointlari

- `GET /` - Asosiy sahifa
- `GET /health` - Sog'liq tekshirish
- `POST /api/medical-query` - Matn orqali tibbiy so'rov yuborish
- `POST /api/voice-query` - Ovoz orqali tibbiy so'rov yuborish

## Testlar

Testlarni ishga tushirish:

```bash
pytest
```
