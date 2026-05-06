# 🚀 Ritesh Kumar - Full Stack Portfolio Technical Documentation

This repository houses a high-performance, responsive portfolio designed with a "Gaming UI" aesthetic (Valorant-inspired). This document explains the technical "why" and "how" behind the code, serving as a guide for the project's architecture.

---

## 🏗️ 1. The Architectural Foundation: The Box Model

The entire portfolio is built on the concept of **Encapsulation**. In web development, we use containers to group logic and styles.

### The `<div>` Tag: The Essential Building Block
* **Role:** A `<div>` (Division) is a non-semantic container. It has no meaning to the browser until we give it a `class` or `id`.
* **Usage:** It is used here to wrap the Profile Image, the About Text, and the Project Cards to treat them as individual "objects" in the layout.

### The `.container` Wrapper: The Global Bound
To prevent the content from stretching infinitely on ultra-wide monitors, a master container is used:
* **Max-Width (900px):** Limits the horizontal spread for better readability (optimal line length).
* **Margin (Auto):** Centers the entire website perfectly in the browser viewport.
* **Padding:** Ensures that on mobile devices, the content doesn't touch the physical edges of the screen.

---

## 📐 2. Advanced Layout System: CSS Flexbox

Instead of old-fashioned floats, this portfolio uses **Flexbox** for dynamic alignment and spacing.

### Key Flexbox Implementations:
1. **The Profile Section (`display: flex`):** This turns the profile area into a flexible row.
2. **Growth Ratios (`flex: 1` vs `flex: 2`):**
    * By assigning `flex: 1` to the **Image** and `flex: 2` to the **Text**, the browser calculates a 1:2 ratio. 
    * **Math:** The text area will always occupy exactly 66.6% of the container, while the image occupies 33.3%.
3. **Adaptive Wrapping (`flex-wrap: wrap`):** * This is the secret to **Responsiveness**. On a phone, the 1:2 ratio is ignored, and the boxes "wrap" to stack vertically, ensuring the user doesn't have to zoom in.

---

## 📝 3. Detailed HTML Content Logic

### 🏷️ Semantic Headers & Sections
* **`<header>`:** Unlike a standard div, the header tag tells search engines (SEO) that this area contains the primary branding and navigation.
* **`<section>`:** Used to divide the page into distinct logical parts (Education, Projects, Contact). This helps screen readers for accessibility.

### 📊 Structured Data (The Education Table)
The education history is displayed using a `<table>` for maximum clarity:
* **`<thead>`:** Separates the labels (Degree, Year) from the data.
* **`border-collapse: collapse`:** A CSS trick used to merge double borders into single, sharp lines for a cleaner look.

### 🛠️ Interactive Elements (The Contact Form)
* **Input Types:** `type="text"` and `type="email"` provide built-in validation.
* **Visual Feedback (`:focus`):** When a user clicks a field, the border changes to the **Primary Red**, indicating the field is "Active."

---

## 🎨 4. Design Systems & Aesthetics

### Theme Variables (`:root`)
The project uses **CSS Variables** to maintain consistency. This allows for a "One-Click Theme Change."
* **Primary Color:** `#ff4655` (Valorant Red)
* **Background:** `#0f172a` (Deep Slate/Navy)

### Visual Polish
* **Glassmorphism Lite:** The project uses `rgba(255, 255, 255, 0.03)` on project cards to create a subtle "see-through" layered effect against the dark background.
* **Depth & Elevation:** `box-shadow` is applied to the main container and profile image to create a 3D sense of depth.
* **Smooth Micro-interactions:** Every link and button features a `0.3s transition`. This prevents "jarring" color changes and makes the UI feel expensive and fluid.

---

## 🔄 5. Project Workflow Summary

The development followed a 4-step logic:
1. **Skeletonization:** Writing clean HTML using semantic tags for SEO.
2. **Containment:** Wrapping logic in the `.container` to maintain a centered, professional flow.
3. **Flex-Alignment:** Using Flexbox to create the 1:2 ratio for the About section and the Grid for the form.
4. **Theming:** Applying global CSS variables and hover states to finalize the "Competitive Gamer" aesthetic.

---
**Maintained by:** Ritesh Kumar  
**Last Updated:** 2026
