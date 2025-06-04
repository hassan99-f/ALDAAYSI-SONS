

```html
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>منيو دعيسي سنظ</title>
  <style>
    body { font-family: sans-serif; padding: 20px; background: #f0f0f0; direction: rtl; text-align: center; }
    input { width: 100%; padding: 10px; margin-bottom: 20px; font-size: 16px; }
    button { display: block; width: 100%; padding: 12px; margin-bottom: 10px; font-size: 16px; background: #28a745; color: white; border: none; cursor: pointer; }
    button:hover { background: #218838; }
  </style>
</head>
<body>

<h2>منيو مطعم دعيسي سنظ</h2>
<input type="text" id="customerName" placeholder="أدخل اسمك هنا" />

<div id="menu"></div>

<script>
const dishes = [
  "بان كيك", "باستا", "وعاء أرز", "كباب",
  "تاكو", "سباغيتي", "سلطة فواكه", "ستيك", "كرات اللحم"
];
const phone = "97334468477"; // بدون +

const menuDiv = document.getElementById("menu");

dishes.forEach(dish => {
  const btn = document.createElement("button");
  btn.innerText = dish;
  btn.onclick = () => {
    const name = document.getElementById("customerName").value.trim();
    if (!name) {
      alert("يرجى إدخال اسم الزبون أولاً");
      return;
    }
