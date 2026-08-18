# Kitoblar katalogi (Library) — React yakuniy imtihon namunasi

Bu loyiha imtihon topshirig'idagi 1-variant ("Kitoblar katalogi") uchun
**namuna** sifatida tayyorlangan. Talab qilingan barcha texnik va
funksional shartlarni qanday amalga oshirish mumkinligini ko'rsatadi.

## Ishga tushirish

1. Bog'liqliklarni o'rnatish:
   ```
   npm install
   ```

2. json-server'ni ishga tushirish (API, 4000-port):
   ```
   npm run server
   ```

3. Boshqa terminalda React ilovasini ishga tushirish:
   ```
   npm run dev
   ```

4. Brauzerda `http://localhost:5173` manzilini oching.

## Loyiha tuzilishi

```
src/
  components/     # Header, Card, Loader, ErrorMessage, Form
  pages/          # HomePage, CatalogPage, ItemDetailPage, AddEditPage, NotFoundPage
  hooks/          # useFetch.js — GET so'rovlar uchun custom hook
  context/        # CartContext.jsx — useContext orqali sevimlilar ro'yxati
  reducers/       # filterReducer.js — useReducer orqali filter/sort/qidiruv
  styles/         # index.css
```

## Talablarning qayerda bajarilgani

| Talab | Qayerda |
|---|---|
| Routing (5 sahifa, dynamic route, 404) | `App.jsx` |
| GET / POST / PUT-PATCH / DELETE | `useFetch.js`, `ItemDetailPage.jsx`, `AddEditPage.jsx` |
| useReducer | `reducers/filterReducer.js`, `CatalogPage.jsx` |
| useContext | `context/CartContext.jsx` |
| Custom hook (2 joyda ishlatilgan) | `hooks/useFetch.js` → `HomePage`, `CatalogPage` |
| Forma va validatsiya | `components/Form.jsx` |
| React.memo / useMemo | `components/Card.jsx` (memo), `pages/CatalogPage.jsx` (useMemo) — sabab kod ichida izohda yozilgan |
| Loader / ErrorMessage | `components/Loader.jsx`, `components/ErrorMessage.jsx` |

## Eslatma o'quvchilar uchun

Bu — **tayyor namuna**, uni nusxalab topshirib bo'lmaydi: har birining
`db.json` fayli, mavzusi va real Git tarixi (12–15 bosqichma-bosqich
commit) o'ziniki bo'lishi shart. Namunadan quyidagilarni o'rganing:

- Har bir komponent nima uchun aynan shu holatni (local yoki global) saqlaydi
- `useFetch` nega alohida faylga chiqarilgan
- `useReducer` va `useContext` qaysi holatlar uchun tanlanganining mantiqi
- `React.memo` va `useMemo` nima uchun aynan shu joyda ishlatilgani (izohlarga qarang)

Himoyada shu savollarning har biriga **o'z so'zlaringiz bilan** javob
bera olishingiz kerak bo'ladi.
