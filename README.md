# GoIT React — Ödev 01: Statik Bileşenler

React bileşenleri, prop'lar ve CSS Modules konularını ele alan ilk React ödevi. Uygulama; kullanıcı profili, arkadaş listesi ve işlem geçmişinden oluşan statik bir profil panosu render eder.

## Uygulama Görünümü

Uygulama üç ana bölümden oluşur:

- **Profil Kartı** — Kullanıcının avatarı, adı, etiketi, konumu ve istatistikleri (takipçi, görüntülenme, beğeni)
- **Arkadaş Listesi** — Her arkadaşın çevrimiçi/çevrimdışı durumunu gösteren kart galerisi
- **İşlem Geçmişi** — Tür, tutar ve para birimi bilgilerini içeren işlem tablosu

## Proje Yapısı

```
src/
├── App.jsx
├── main.jsx
├── index.css
├── components/
│   ├── Profile/
│   │   ├── Profile.jsx
│   │   └── Profile.module.css
│   ├── FriendList/
│   │   ├── FriendList.jsx
│   │   └── FriendList.module.css
│   ├── FriendListItem/
│   │   ├── FriendListItem.jsx
│   │   └── FriendListItem.module.css
│   └── TransactionHistory/
│       ├── TransactionHistory.jsx
│       └── TransactionHistory.module.css
└── data/
    ├── userData.json
    ├── friends.json
    └── transactions.json
```

## Bileşenler

### `Profile`
Kullanıcı profil kartını render eder.

| Prop | Tür | Açıklama |
|---|---|---|
| `name` | `string` | Kullanıcı adı |
| `tag` | `string` | Kullanıcı etiketi |
| `location` | `string` | Konum bilgisi |
| `image` | `string` | Avatar URL'si |
| `stats` | `object` | `followers`, `views`, `likes` alanlarını içerir |

### `FriendList`
Arkadaş listesini render eder.

| Prop | Tür | Açıklama |
|---|---|---|
| `friends` | `array` | Arkadaş nesnelerinden oluşan dizi |

### `FriendListItem`
Tek bir arkadaş kartını render eder.

| Prop | Tür | Açıklama |
|---|---|---|
| `avatar` | `string` | Avatar URL'si |
| `name` | `string` | Arkadaşın adı |
| `isOnline` | `boolean` | Çevrimiçi durumu |

### `TransactionHistory`
İşlem geçmişi tablosunu render eder.

| Prop | Tür | Açıklama |
|---|---|---|
| `items` | `array` | `id`, `type`, `amount`, `currency` alanlarını içeren işlem dizisi |

## Başlarken

```bash
npm install
npm run dev
```

## Komutlar

| Komut | Açıklama |
|---|---|
| `npm run dev` | Geliştirme sunucusunu başlatır |
| `npm run build` | Prodüksiyon için derleme yapar |
| `npm run preview` | Prodüksiyon derlemesini önizler |
| `npm run lint` | ESLint çalıştırır |

## Teknolojiler

- [React 19](https://react.dev/)
- [Vite](https://vite.dev/)
- CSS Modules
