# ElevenLabs Proxy for Bloom English

Bu proxy, ElevenLabs API'yi CORS sorunu olmadan kullanmak için.

## Kurulum

1. Bu repo'yu GitHub'a yükle
2. Vercel'de "New Project" → GitHub repo'yu seç
3. Environment Variables ekle:
   - `ELEVENLABS_API_KEY` = `sk_3fc96cd83841e388a321e93b9792c1aadf7d1955e1d74753`
4. Deploy

## Kullanım

```javascript
const response = await fetch('https://YOUR-PROJECT.vercel.app/api/tts', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ text: 'Hello world' })
});
const audioBlob = await response.blob();
const audio = new Audio(URL.createObjectURL(audioBlob));
audio.play();
```
