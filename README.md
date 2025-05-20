npm start

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

#  React + Firebase Chat Uygulaması

Bu proje, **React.js** ve **Firebase** kullanılarak geliştirilen kullanıcı doğrulamalı bir sohbet uygulamasıdır. Kullanıcılar sisteme kayıt olabilir, e-posta doğrulaması yapabilir, giriş yapabilir, şifrelerini sıfırlayabilir ve oturum açtıktan sonra sohbet odasına erişebilirler.

##  Özellikler

-  E-posta & şifre ile kullanıcı kaydı
-  E-posta doğrulama kontrolü (doğrulanmayan kullanıcılar giriş yapamaz)
-  Giriş yapma ve çıkış yapma işlemleri
-  Şifre sıfırlama (e-posta ile bağlantı gönderimi)
-  1 saat sonunda otomatik oturum kapatma
-  Firebase Authentication & Firestore entegrasyonu
-  React Router ile sayfa yönlendirme
-  Temel kullanıcı arayüzü ve form validasyonu

##  Kullanılan Teknolojiler

- [React.js](https://reactjs.org/)
- [Firebase Authentication](https://firebase.google.com/docs/auth)
- [Firebase Firestore](https://firebase.google.com/docs/firestore)
- [React Router v6](https://reactrouter.com/en/main)

##  Proje Yapısı
src/
├── firebase/
│ └── firebaseConfig.js # Firebase yapılandırması (auth & firestore)
├── pages/
│ ├── Home.js # Anasayfa, yönlendirme içerir
│ ├── Login.js # Giriş formu
│ ├── Register.js # Kayıt formu (doğrulama içerir)
│ ├── ChatRoom.js # Sohbet odası (1 saatlik oturum)
│ └── ResetPassword.js # Şifre sıfırlama formu
└── App.js # Rotaların tanımlandığı ana bileşen


##  Kurulum ve Çalıştırma

1. Bu repoyu klonlayın:
    ```bash
    git clone https://github.com/kullanici-adi/proje-adi.git
    cd proje-adi
    ```

2. Bağımlılıkları yükleyin:
    ```bash
    npm install
    ```

3. Firebase projesi oluşturun ve `firebaseConfig.js` dosyasına kendi yapılandırmanızı yapıştırın:
    ```js
    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_PROJECT_ID.appspot.com",
      messagingSenderId: "SENDER_ID",
      appId: "APP_ID"
    };
    ```

4. Uygulamayı başlatın:
    ```bash
    npm start
    ```

##  Firebase Neden Kullanıldı?

Firebase, uygulamamızda kullanıcı yönetimini (kayıt, giriş, doğrulama, şifre sıfırlama), veritabanı işlemlerini ve oturum sürelerini kolayca ve güvenli biçimde yönetebilmemizi sağlar.

Bu projede şu amaçlarla kullanıldı:

- **Authentication**: E-posta ile kullanıcı kimlik doğrulama.
- **Email Verification**: Güvenliği artırmak için kullanıcı e-posta doğrulaması.
- **Password Reset**: Firebase’in sağladığı hazır e-posta şablonlarıyla şifre sıfırlama.
- **Session Handling**: Giriş yapan kullanıcılar için zamanlı oturum süresi kontrolü.
- **Firestore (Opsiyonel)**: Sohbet verilerinin bulut veritabanında tutulması için altyapı.



>  Proje: React + Firebase ile basit, güvenli ve doğrulamalı bir sohbet uygulaması





