# ⚛️ React Toolkit – أساسيات وأوامر مهمة

دليل مختصر ومنظم لأهم أساسيات React والأوامر الشائعة، مناسب ترفعه مباشرة على GitHub كـ **README.md**.

---

## 1️⃣ إنشاء مشروع React

### باستخدام Vite (الأفضل والأسرع)
```bash
npm create vite@latest my-app
cd my-app
npm install
npm run dev
```

### باستخدام Create React App (قديم نسبيًا)
```bash
npx create-react-app my-app
cd my-app
npm start
```

---

## 2️⃣ هيكلة المشروع الأساسية

```text
src/
 ├─ assets/
 ├─ components/
 ├─ pages/
 ├─ App.jsx
 ├─ main.jsx
```

---

## 3️⃣ أساسيات React

### Component
```jsx
function App() {
  return <h1>Hello React</h1>;
}
export default App;
```

### JSX
- كتابة HTML داخل JavaScript
- يجب إرجاع عنصر واحد فقط

---

## 4️⃣ Hooks الأساسية

### useState
```jsx
import { useState } from "react";

const [count, setCount] = useState(0);
```

### useEffect
```jsx
import { useEffect } from "react";

useEffect(() => {
  console.log("Component Mounted");
}, []);
```

---

## 5️⃣ التعامل مع الفورم

```jsx
const [form, setForm] = useState({ name: "", password: "" });

const handleChange = (e) => {
  setForm({ ...form, [e.target.name]: e.target.value });
};
```

---

## 6️⃣ React Router

### التثبيت
```bash
npm install react-router-dom
```

### الاستخدام
```jsx
import { BrowserRouter, Routes, Route } from "react-router-dom";
```

---

## 7️⃣ Styling

### CSS
```jsx
import './App.css';
```

### Bootstrap
```bash
npm install bootstrap
```

### Tailwind
```bash
npm install -D tailwindcss
npx tailwindcss init
```

---

## 8️⃣ إدارة البيانات

- Props
- State
- Lifting State Up
- Context API

---

## 9️⃣ Fetch API

```jsx
useEffect(() => {
  fetch("https://api.example.com/data")
    .then(res => res.json())
    .then(data => console.log(data));
}, []);
```

---

## 🔟 أوامر npm المهمة

```bash
npm install        # تثبيت الحزم
npm run dev        # تشغيل المشروع
npm run build      # build للإنتاج
```

---

## 📌 نصائح

- قسم المشروع Components و Pages
- استخدم reusable components
- التزم بتسمية واضحة للملفات

---

## 📂 جاهز للرفع على GitHub

- احفظ الملف باسم `README.md`
- أضف Screenshots للمشروع
- أضف وصف بسيط للمشروع

---

✨ **بالتوفيق في رحلتك مع React**

