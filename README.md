# 🏞️ Visit Namibia - Responsive CSS Grid Web Page

This project is a simple and visually engaging web page that promotes Namibia as a travel destination. It demonstrates how to use **CSS Grid** to create a responsive, mobile-friendly layout adaptable to various screen sizes, including desktop, tablet, and mobile devices.

---

## 📌 Features
- Responsive layout using **CSS Grid**
- Fluid design for mobile, tablet, and PC screens
- Highlighted sections for featured content
- Image and text pairings optimized for various viewports
- Clean, modern typography using Google Fonts

---

## 🧱 CSS Grid Layout

The core of this project’s responsiveness lies in **CSS Grid**, which was used to build a structured and flexible layout for the main content area.

### 🖥️ Desktop (≥ 980px)

- The `.grid-container` uses a `grid-template-columns: 1fr 1fr 1fr` layout to display articles in a **3-column layout**.
- The `.featured` article (The first Section on the site page) spans **all 3 columns** and uses a **nested grid** to place image and text side-by-side.
![image](https://github.com/user-attachments/assets/d39ea91e-8445-4021-9516-302bbf5d2c80)


### 📱 Tablet (≤ 980px)

- All articles, including the `.featured` article, span all columns using `grid-column: span 3`.
- Each article switches to a **2-column grid** layout: image and text placed side-by-side.
![image](https://github.com/user-attachments/assets/a1a3220c-6b7f-4b16-9475-568b825bd597)


### 📲 Mobile (≤ 760px)

- The layout switches to **block-level stacking** using `display: block`, ensuring that each article's content is stacked vertically.
- Margins are adjusted for smaller screens to maintain readability.
![image](https://github.com/user-attachments/assets/df0d5c90-3127-4280-ac78-9f62d77868fc)


---

## 🖼️ Layout Highlights

### HTML Structure

- Uses semantic elements: `<header>`, `<main>`, `<article>`, and `<img>`
- Clean and accessible layout with descriptive text

### CSS Styling

- Utilizes `@media` queries for breakpoints at **980px** and **760px**
- Applies `grid-column: span 3` and `grid-template-columns` to dynamically adapt the layout
- Enhanced aesthetics with rounded borders, gaps, and padding

---

##  Code Snippets

### ✅ CSS Grid Container

```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 60px;
    max-width: 1200px;
    margin: 20px auto;
}
```

## ✅ Featured Article Nested Grid
```css
article.featured {
    grid-column: span 3;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
}
```
## ✅ Media Query for Tablet
```css
@media screen and (max-width: 980px) {
    article {
        grid-column: span 3;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 60px;
        align-items: center;
    }
}
```
## ✅ Media Query for Mobile
```css
@media screen and (max-width: 760px) {
    article, article.featured {
        display: block;
        margin: 0 20px;
    }
}
```
## 📁 Project File Structure
```text
visit-namibia/
├── index.html # Main HTML file
├── styles.css # CSS file using Grid for layout & responsiveness
├── README.md # Project documentation in Markdown
├── images/ # Image assets
│ ├── nami.png # Favicon
│ ├── nam.jpg # Featured desert image
│ ├── bird.jpg # Bird sighting image
│ ├── spring.jpg # Springbok image
│ └── zebra.jpg # Zebra image


