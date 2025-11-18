# TechCon 2024 — HTML Website

A 5-page, standards-compliant website for the TechCon 2024 conference.  
Focus: clean HTML structure, accessible content, working navigation, forms, tables, media embeds.

---

## 🎯 Project Goals

By completing this project you will:
- Structure pages with semantic HTML (`header`, `nav`, `main`, `section`, `article`, `footer`).
- Organize content with headings (`h1`–`h6`), paragraphs, and lists.
- Build internal navigation with links.
- Present a conference schedule in an accessible **table**.
- Create **forms** for registration and contact (with basic HTML validation).
- Add **images** with `alt`, an embedded **map** (`iframe`), and an optional **promo video** (`video`).

> Scope emphasis: HTML first. You can add light CSS/JS later, but the deliverable must stand on HTML alone.

---

## 📁 Structure

```text
techcon-2024/
├─ index.html # Homepage
├─ about.html # About TechCon (history, mission, speakers)
├─ schedule.html # Detailed schedule (table)
├─ register.html # Registration form
└─ contact.html # Contact info, socials, map, contact form (+ optional video)

---

## 🧭 Page Requirements

### 1) `index.html` — Homepage
- Hero title (e.g., “TechCon 2024”).
- Short intro paragraph and date/location.
- Clear navigation to all other pages.
- Optional highlights (key tracks, keynote teaser).

### 2) `about.html` — About
- Headings for **History**, **Mission**, **Notable Speakers**.
- Speaker list (names + short bios). Use semantic lists/sections.

### 3) `schedule.html` — Schedule (Table)
- Use `<table>` with:
  - `<caption>` describing the table.
  - `<thead>` with column headings (e.g., Time, Session, Speaker, Room/Track).
  - `<tbody>` with rows for sessions.
  - Consider `scope="col"` on `<th>` and consistent time formatting.
- Optional: split by day with multiple tables or sectional headings.

### 4) `register.html` — Registration Form
- `<form>` with labeled controls:
  - Name (text), Email (email), Password (password),
  - Ticket type (select or radios),
  - Interests (checkboxes),
  - Terms of service (required checkbox),
  - Submit button.
- Use `required`, `minlength`, etc., where sensible.
- No backend needed—focus on HTML semantics and built-in validation.

### 5) `contact.html` — Contact & Map
- Contact details (email, phone, address).
- Social links (LinkedIn/X/Facebook/YouTube) with clear text labels.
- **Map embed** using `<iframe>` (Google Maps share → embed HTML).
- “Contact Us” form (name, email, message; all labeled).
- Optional: conference promo **video** via `<video>` with `controls` and fallback text.

---

## Navigation (All Pages)

- A consistent `<header>` + `<nav>` with a list of links to:
  - Home (`index.html`)
  - About (`about.html`)
  - Schedule (`schedule.html`)
  - Register (`register.html`)
  - Contact (`contact.html`)

Keep link text descriptive (e.g., “About TechCon” vs. “About”).

---

## Accessibility & Quality Checklist

- Semantic landmarks: `header`, `nav`, `main`, `footer`.
- One top-level `<h1>` per page; nested headings are hierarchical.
- Every image has meaningful `alt` (or `alt=""` if purely decorative).
- Forms:
  - Each input has a `<label for="...">` with a matching `id`.
  - Use `required`, `type="email"`, `minlength`, `maxlength` appropriately.
  - Group related options with `<fieldset><legend>…</legend>…</fieldset>`.
- Tables:
  - Use `<caption>`, `<thead>`, `<tbody>`, `<th scope="col|row">` where relevant.
- Links:
  - Descriptive text (avoid “click here”).
  - External links may use `target="_blank"` plus `rel="noopener"`.
- Validate HTML with W3C Validator (fix errors/warnings).

---

## Getting Started

1. Create the folder structure above.
2. Build each page with semantic HTML and internal links.
3. Open pages directly in your browser or via a simple local server.
4. Validate HTML here: <https://validator.w3.org/>

---

## Snippets

### Minimal page shell
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TechCon 2024 — Page Title</title>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="schedule.html">Schedule</a></li>
        <li><a href="register.html">Register</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <!-- page-specific content -->
  </main>

  <footer>
    <p>&copy; 2025 TechCon. All rights reserved.</p>
  </footer>
</body>
</html>
