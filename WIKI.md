# REACT-FORMS Wiki

## 📋 İçindekiler / Table of Contents
- [Proje Hakkında](#proje-hakkında)
- [Özellikler](#özellikler)
- [Teknoloji Yığını](#teknoloji-yığını)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Proje Yapısı](#proje-yapısı)
- [Geliştirme](#geliştirme)
- [Mevcut Scriptler](#mevcut-scriptler)
- [Form Validasyonu](#form-validasyonu)

---

## 🎯 Proje Hakkında

REACT-FORMS, React Router DOM kullanarak form yönetimi ve validasyonu gösteren modern bir React TypeScript uygulamasıdır. Proje, kullanıcı girişlerini toplama, doğrulama ve yönlendirme işlemlerini içerir.

### About the Project

REACT-FORMS is a modern React TypeScript application demonstrating form management and validation using React Router DOM. The project includes collecting user inputs, validation, and routing functionality.

---

## ✨ Özellikler / Features

- ✅ **React Router DOM** ile sayfa yönlendirme
- ✅ **TypeScript** ile tip güvenliği
- ✅ **Tailwind CSS** ile modern ve responsive tasarım
- ✅ **Form Validasyonu** (required fields, email pattern validation)
- ✅ İletişim formu ile kullanıcı bilgisi toplama
- ✅ Form gönderimi sonrası teşekkür sayfası
- ✅ Tailwind Forms plugin ile gelişmiş form stilleri

---

## 🛠 Teknoloji Yığını / Tech Stack

### Ana Teknolojiler / Core Technologies
- **React** v18.2.0 - UI kütüphanesi
- **TypeScript** v4.9.5 - Tip güvenliği
- **React Router DOM** v6.14.2 - Routing yönetimi

### Styling
- **Tailwind CSS** v3.3.3 - Utility-first CSS framework
- **@tailwindcss/forms** v0.5.4 - Form stilleri için plugin
- **Autoprefixer** v10.4.14 - CSS uyumluluğu

### Testing
- **@testing-library/react** v13.4.0
- **@testing-library/jest-dom** v5.17.0
- **@testing-library/user-event** v13.5.0

### Build Tools
- **React Scripts** v5.0.1 - Create React App build konfigürasyonu

---

## 📦 Kurulum / Installation

### Gereksinimler / Prerequisites
- Node.js (v16 veya üzeri)
- npm veya yarn

### Adımlar / Steps

1. **Projeyi klonlayın / Clone the repository:**
```bash
git clone https://github.com/C8338Soner/REACT-FORMS.git
cd REACT-FORMS/react-forms
```

2. **Bağımlılıkları yükleyin / Install dependencies:**
```bash
npm install
```

3. **Tailwind CSS kurulumu / Tailwind CSS setup:**

Tailwind CSS bağımlılıkları:
```bash
npm i -D tailwindcss
npm i -D autoprefixer
npm i -D @tailwindcss/forms
npx tailwindcss init -p
```

4. **index.css dosyasını güncelleyin / Update index.css:**

`src/index.css` dosyasının en üstüne şunları ekleyin:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5. **Uygulamayı başlatın / Start the application:**
```bash
npm start
```

Uygulama [http://localhost:3000](http://localhost:3000) adresinde açılacaktır.

---

## 🚀 Kullanım / Usage

### Ana Sayfa / Home Page
- Uygulama başladığında otomatik olarak `/contact` sayfasına yönlendirilirsiniz.

### İletişim Formu / Contact Form
**Endpoint:** `/contact`

Form alanları:
- **Ad (Name):** Zorunlu metin alanı
- **E-posta (Email):** Zorunlu, geçerli email formatında olmalı
- **İletişim Nedeni (Reason):** Zorunlu seçim alanı
  - Support (Destek)
  - Feedback (Geri Bildirim)
  - Other (Diğer)
- **Ek Notlar (Notes):** Opsiyonel metin alanı

### Teşekkür Sayfası / Thank You Page
**Endpoint:** `/thank-you/:name`

Form başarıyla gönderildikten sonra, kullanıcı adıyla birlikte teşekkür mesajı gösterilir.

---

## 📁 Proje Yapısı / Project Structure

```
react-forms/
├── public/
│   ├── index.html
│   └── manifest.json
├── src/
│   ├── App.tsx              # Ana uygulama bileşeni ve routing
│   ├── ContactPage.tsx      # İletişim formu sayfası ve action
│   ├── ThankYouPage.tsx     # Teşekkür sayfası
│   ├── App.css              # Global stiller
│   ├── index.tsx            # Uygulama giriş noktası
│   ├── App.test.tsx         # Test dosyası
│   ├── setupTests.ts        # Test kurulumu
│   ├── reportWebVitals.ts   # Performans metrikleri
│   └── react-app-env.d.ts   # TypeScript tanımlamaları
├── package.json             # Proje bağımlılıkları
├── tsconfig.json           # TypeScript konfigürasyonu
├── tailwind.config.js      # Tailwind CSS konfigürasyonu
├── postcss.config.js       # PostCSS konfigürasyonu
└── .prettierrc.json        # Prettier konfigürasyonu
```

### Önemli Dosyalar / Key Files

#### App.tsx
Ana routing mantığını içerir:
- `/` → `/contact` yönlendirmesi
- `/contact` → İletişim formu
- `/thank-you/:name` → Teşekkür sayfası

#### ContactPage.tsx
- **ContactPage Component:** Form UI'ı
- **contactPageAction:** Form submit işlemi ve redirect

#### ThankYouPage.tsx
- Form gönderimi sonrası gösterilen başarı sayfası
- URL parametresinden kullanıcı adını alır

---

## 💻 Geliştirme / Development

### Kod Stili / Code Style
Proje Prettier ile formatlanmıştır. Konfigürasyon `.prettierrc.json` dosyasında bulunur.

### TypeScript
Proje tamamen TypeScript ile yazılmıştır. Type definitions:
```typescript
type Contact = {
  name: string;
  email: string;
  reason: string;
  notes: string;
};
```

### Tailwind CSS Kullanımı
Utility-first yaklaşımı ile stil uygulanır:
```jsx
<div className="flex flex-col py-10 max-w-md mx-auto">
  {/* İçerik */}
</div>
```

### Form Handling
React Router DOM'un `Form` ve `action` özellikleri kullanılır:
```jsx
<Form method="post">
  {/* Form alanları */}
</Form>
```

---

## 📜 Mevcut Scriptler / Available Scripts

### `npm start`
Geliştirme modunda uygulamayı başlatır.
- Otomatik sayfa yenileme
- Tarayıcıda [http://localhost:3000](http://localhost:3000) açılır

### `npm test`
Test runner'ı interaktif watch modunda başlatır.

### `npm run build`
Production için optimize edilmiş build oluşturur.
- `build` klasörüne çıktı verir
- Minified ve optimize edilmiş dosyalar
- Production'a hazır

### `npm run eject`
⚠️ **Dikkat:** Bu işlem geri alınamaz!
- Create React App konfigürasyonunu açığa çıkarır
- Tam kontrol sağlar ancak karmaşıklığı artırır

---

## 🔒 Form Validasyonu / Form Validation

### İstemci Tarafı Validasyon / Client-side Validation

1. **Required Fields:**
   - Name (Ad)
   - Email (E-posta)
   - Reason (Neden)

2. **Email Pattern Validation:**
```jsx
<input 
  type="email" 
  pattern='\S+@\S+\.\S+' 
  required 
/>
```

3. **Select Validation:**
Kullanıcı bir neden seçmelidir (boş değer kabul edilmez).

### Form Submit İşlemi

```typescript
export async function contactPageAction({ request }: ActionFunctionArgs) {
  const formData = await request.formData();
  const contact = {
    name: formData.get('name'),
    email: formData.get('email'),
    reason: formData.get('reason'),
    notes: formData.get('notes'),
  } as Contact;
  console.log('Submitted details:', contact);
  return redirect(`/thank-you/${formData.get('name')}`);
}
```

---

## 🤝 Katkıda Bulunma / Contributing

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request açın

---

## 📄 Lisans / License

Bu proje özel bir projedir.

---

## 👤 Geliştirici / Developer

**C8338Soner**
- GitHub: [@C8338Soner](https://github.com/C8338Soner)

---

## 📚 Kaynaklar / Resources

- [React Documentation](https://react.dev/)
- [React Router DOM](https://reactrouter.com/)
- [TypeScript Documentation](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Create React App](https://create-react-app.dev/)

---

## 🐛 Bilinen Sorunlar / Known Issues

Şu anda bilinen bir sorun yoktur.

---

## 🔄 Gelecek Geliştirmeler / Future Enhancements

- [ ] Backend entegrasyonu
- [ ] Form verilerini veritabanına kaydetme
- [ ] E-posta bildirimleri
- [ ] Çoklu dil desteği (i18n)
- [ ] Form state yönetimi (React Hook Form veya Formik)
- [ ] Server-side validasyon
- [ ] Gelişmiş hata yönetimi
- [ ] Unit ve integration testlerinin artırılması

---

**Son Güncelleme / Last Updated:** 2026-02-22
