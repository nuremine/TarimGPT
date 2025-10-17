# 🌾 TarımGPT: Çiftçinin Dijital Asistanı (Yapay Zekalı Sürüm)
# Geliştirici: Emine Nur Aba 💚
# Akbank Generative AI Bootcamp Projesi

import streamlit as st
from dotenv import load_dotenv
import os
from openai import OpenAI

# .env dosyasını yükle
load_dotenv()
api_key = os.getenv("OPENAI_API_KEY")

# OpenAI istemcisi oluştur
client = OpenAI(api_key=api_key)

# Streamlit ayarları
st.set_page_config(page_title="TarımGPT", page_icon="🌾", layout="centered")
st.title("🌾 TarımGPT: Çiftçinin Dijital Asistanı")
st.write("Merhaba 👩‍🌾 Ben TarımGPT. Tarım, bitki bakımı ve ziraat konularında sana yardımcı olabilirim!")

# Kullanıcıdan girdi al
user_input = st.text_input("Sormak istediğin bir şey var mı?", placeholder="Örn: Mısır ne zaman sulanmalı?")

# Kullanıcı soru yazarsa yanıt üret
if user_input:
    with st.spinner("Yanıt hazırlanıyor..."):
        try:
            response = client.chat.completions.create(
                model="gpt-3.5-turbo",
                messages=[
                    {"role": "system", "content": "Sen akıllı bir tarım danışmanısın. Türkçe konuş ve sade, kısa yanıtlar ver."},
                    {"role": "user", "content": user_input}
                ]
            )
            answer = response.choices[0].message.content
            st.success("🤖 TarımGPT: " + answer)
        except Exception as e:
            st.error("Bir hata oluştu. Lütfen API anahtarını kontrol et.")
            st.caption(f"Hata detayı: {e}")

st.markdown("---")
st.caption("📘 Akbank GenAI Bootcamp | TarımGPT © 2025 Emine Nur Aba")
