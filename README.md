
<img width="1815" height="872" alt="image" src="https://github.com/user-attachments/assets/e5e7e614-c7f6-410c-95d0-60251f1aadb3" />


---

````markdown
# 🛒 Angular 15 Product Showcase App

This is a simple **Angular 15** application that:

- ✅ Fetches products from a public API
- ✅ Displays them in a grid layout
- ✅ Allows real-time search filtering
- ✅ Uses Tailwind CSS for styling

---





## ✨ Features

- 🧩 **Angular 15** used via local CLI (`npx -p @angular/cli@15`)
- 🌐 Fetches product data from [Fake Store API](https://fakestoreapi.com/)
- 🎨 Styled beautifully with Tailwind CSS
- 🔍 Live search functionality
- 🧱 Responsive product grid layout

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/product-app.git
cd product-app
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Run the App (Locally Using Angular 15 CLI)

```bash
npx ng serve
```

Visit: [http://localhost:4200](http://localhost:4200)

---

## 📦 Project Setup (If Starting Fresh)

### 1. Create Angular 15 Project

```bash
npx -p @angular/cli@15 ng new product-app
cd product-app
```

### 2. Install Tailwind CSS

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

Update `tailwind.config.js`:

```js
module.exports = {
  content: ["./src/**/*.{html,ts}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

Add Tailwind to `src/styles.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 📁 File Structure

```
product-app/
│
├── src/
│   ├── app/
│   │   ├── product-list/
│   │   │   ├── product-list.component.ts
│   │   │   ├── product-list.component.html
│   │   ├── product.service.ts
│   │   └── app.component.ts/html
│
├── tailwind.config.js
├── angular.json
├── package.json
└── styles.css
```

---

## 🔧 Core Code Highlights

### `product.service.ts`

Fetches data from Fake Store API:

```ts
getProducts(): Observable<any[]> {
  return this.http.get<any[]>('https://fakestoreapi.com/products');
}
```

### `product-list.component.ts`

Handles search/filter logic:

```ts
filterProducts(): void {
  this.filteredProducts = this.products.filter((product) =>
    product.title.toLowerCase().includes(this.searchTerm.toLowerCase())
  );
}
```

---

## 🧪 Test It

Try searching:

* `"shirt"`
* `"cotton"`
* `"jacket"`
* `"bag"`

You'll see real-time filtering in action.

---

## 🌐 API Used

[FakeStoreAPI](https://fakestoreapi.com/) — A free dummy product API with images, descriptions, and prices.

---

## 🛠 Tech Stack

* Angular 15 (via local CLI)
* Tailwind CSS
* TypeScript
* RxJS
* Fake Store API

---

## 💡 Notes on Angular CLI

If you have **Angular CLI v19** globally, no problem!

Angular uses the local CLI inside the project folder.

✅ Run locally using:

```bash
npx ng serve
```

---

---


