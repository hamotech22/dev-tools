# 🚀 Tailwind CSS – Structure & Quick Cheatsheet

## 🧱 الشكل العام لأي صفحة (Base Structure)

ده أبسط هيكل HTML ممكن تبدأ بيه أي مشروع Tailwind.
- `body` فيه ألوان عامة للموقع
- `container` بيوسّط المحتوى
- `p-4` بيدي مسافة داخلية

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tailwind App</title>
</head>
<body class="bg-gray-100 text-gray-800">

  <div class="container mx-auto p-4">
    <h1 class="text-3xl font-bold text-center mb-4">
      Hello Tailwind
    </h1>

    <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded">
      Click Me
    </button>
  </div>

</body>
</html>
```

---

## 🔹 أهم الكلاسات (مختصر مفيد)

الكلاسات دي هي أكتر حاجة هتستخدمها يوميًا وانت شغال Tailwind.

### 🎨 الألوان
بتستخدمها لتغيير لون الخلفية، النص، أو البوردر.
```txt
bg-red-500
text-gray-700
border-blue-300
```

---

### 📏 المسافات (Padding & Margin)
بتتحكم في المسافات الداخلية والخارجية للعناصر.
```txt
p-4        → padding
px-4 py-2  → padding أفقي / رأسي
m-4        → margin
mt-2 mb-6 → margin top / bottom
```

---

### 🧱 العرض والارتفاع
بتحدد حجم العنصر بالنسبة للشاشة أو العنصر الأب.
```txt
w-full
w-1/2
h-screen
max-w-lg
```

---

### 🖋️ النصوص
بتتحكم في حجم الخط، سمكه، ومحاذاته.
```txt
text-sm | text-lg | text-3xl
font-bold | font-medium
text-center | text-right
uppercase
```

---

### 🧭 Flexbox (مهم جدًا)
بيستخدم لترتيب العناصر جنب بعض أو فوق بعض بسهولة.
```txt
flex
items-center
justify-between
justify-center
gap-4
```

**مثال:**
```html
<div class="flex items-center justify-between">
  <span>Logo</span>
  <button>Login</button>
</div>
```

---

### 📐 Grid
مناسب لتقسيم الصفحة أو عرض كروت بشكل منظم.
```txt
grid
grid-cols-3
gap-4
```

---

### 🟦 الحدود والظل
بتدي شكل أنضف وعمق للعناصر زي الكروت.
```txt
rounded
rounded-lg
border
shadow
shadow-md
```

---

### 🎭 Hover & Transition
بتستخدم لتأثيرات الحركة عند المرور بالماوس.
```txt
hover:bg-blue-600
transition
duration-300
```

---

### 📱 Responsive (مهم)
بتخلي الموقع شكله مظبوط على الموبايل والتابلت والديسكتوب.
```txt
sm:text-sm
md:text-lg
lg:text-2xl
xl:grid-cols-4
```

**مثال:**
```html
<h1 class="text-lg md:text-2xl lg:text-4xl">
  Responsive Text
</h1>
```

---

## 🃏 مثال كارت جاهز (Reusable Card)
كارد بسيط تقدر تعيد استخدامه في أي مشروع (منتجات – مستخدمين – مقالات).

```html
<div class="bg-white rounded-lg shadow p-4 max-w-sm">
  <h2 class="text-xl font-bold mb-2">Card Title</h2>
  <p class="text-gray-600 mb-4">
    This is a simple card using Tailwind.
  </p>
  <button class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">
    Action
  </button>
</div>
```

---

## 🧠 الخلاصة
ملخص سريع يثبت الفكرة الأساسية لتايلويند.
- Tailwind بيعتمد على **Utility Classes**
- مفيش `row` و `col` زي Bootstrap
- Flex و Grid هما الأساس
- الملف ده مناسب كـ **Reference سريع** لأي مشروع

---

> ✅ جاهز للرفع مباشرة على GitHub كملف Markdown

