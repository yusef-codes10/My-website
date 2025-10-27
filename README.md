# My Website Prototype

## Overview

## 🔥 Preview

![Nova Rebooted Screenshot](/images/demo.png)

This is the prototyped version of my personal website. It was built entirely with **HTML and CSS** for now, focusing on layout, structure, and basic interactivity. The design is inspired by Charlene’s clean and minimal aesthetic.

---

## What I Learned Today

### 1. Using `transition` and `transform: scale()` Correctly

* Learned how to use CSS **transitions** with **transform scale** to create smooth hover animations.
* Important takeaway: **Avoid using width or height changes** for hover effects since they cause layout shifts.
* Using `transform: scale()` allows for animations that **don’t affect the element’s box size**, keeping the layout stable.

```css
.action i {
  transition: transform 0.3s ease;
}

.action i:hover {
  transform: scale(1.2);
}
```

---

### 2. Understanding `display: inline-block` vs `display: block`

* The **`.action`** class uses `display: inline-block` to keep icons and labels aligned horizontally while allowing block-like control (like padding or margin).
* Inside each `.action`, the **`i` tag** (icon) uses `display: block` to force the icon to appear above its label.

```css
.action {
  display: inline-block;
  text-align: center;
}

.action i {
  display: block;
}
```

This is what makes the icon and its text (`<span>`) appear in a **stacked vertical layout**.

---

### 3. Adding Labels to Icons

* Icons are wrapped in a parent `.action` container with an accompanying `<span>` label:

```html
<div class="action">
  <i class="bi bi-envelope-paper"></i>
  <span>Contact</span>
</div>
```

This gives each icon a textual label that describes its function — similar to labeling form inputs.

---

### 4. Structuring the Hero Section

* The hero section takes the full viewport height (`100vh`) and uses a **fixed background** for a subtle parallax effect.

```css
.hero-section {
  height: 100vh;
  background: url(./images/green.png) center / cover no-repeat;
  background-attachment: fixed;
}
```

---

### 5. Using Bootstrap Icons

* Integrated **Bootstrap Icons** via CDN.
* Adjusted icon sizes with the `font-size` property (e.g., `1.8rem`).
* Used consistent spacing and alignment to create a clean and minimal icon-based navigation and action area.

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.13.1/font/bootstrap-icons.min.css" />
```

---

## Notes for Future Versions

* Add interactivity with **JavaScript** (e.g., toggling light/dark modes, muting sounds, switching icons).
* Replace placeholder images with real assets.
* Implement responsive design for smaller screens.
* Possibly recreate this layout later with a **grid system** or **flexbox refinement**.

---

## File Structure

```
project-root/
├── index.html
├── styles.css
├── images/
│   └── green.png
└── README.md
```

## 👨‍💻 Author

**Yusef Codes**
