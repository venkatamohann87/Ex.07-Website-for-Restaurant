# Ex.07 Restaurant Website
## Date: 07.12.2024

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    background: radial-gradient(circle at top left, #ffedd5, #fee2e2, #e0f2fe);
    color: #0f172a;
    min-height: 100vh;
}

a {
    text-decoration: none;
    color: inherit;
}

img {
    max-width: 100%;
    display: block;
}

.page {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 1.5rem;
}

/* NAVBAR */

.navbar {
    position: sticky;
    top: 0;
    z-index: 50;
    backdrop-filter: blur(16px);
    background: rgba(15,23,42,0.75);
    color: #e5e7eb;
    box-shadow: 0 18px 45px rgba(15,23,42,0.35);
}

.nav-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
}

.brand {
    display: flex;
    align-items: center;
    gap: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-size: 0.95rem;
}

.brand-mark {
    width: 36px;
    height: 36px;
    border-radius: 999px;
    border: 2px solid rgba(248,250,252,0.8);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1rem;
    background: radial-gradient(circle at 20% 0%, #f97316, #b91c1c);
    color: #f9fafb;
    box-shadow: 0 8px 18px rgba(0,0,0,0.35);
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 1.2rem;
    font-size: 0.95rem;
}

.nav-link {
    position: relative;
    padding: 0.3rem 0;
    opacity: 0.85;
    transition: all 0.2s ease;
}

.nav-link::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -0.15rem;
    width: 0;
    height: 2px;
    border-radius: 999px;
    background: linear-gradient(to right, #f97316, #facc15);
    transition: width 0.2s ease;
}

.nav-link:hover {
    opacity: 1;
    transform: translateY(-1px);
}

.nav-link:hover::after {
    width: 100%;
}

.nav-link.active {
    opacity: 1;
    font-weight: 600;
}

.nav-link.active::after {
    width: 100%;
}

.nav-cta {
    padding: 0.45rem 0.95rem;
    border-radius: 999px;
    border: 1px solid rgba(248,250,252,0.5);
    font-size: 0.85rem;
    display: flex;
    gap: 0.4rem;
    align-items: center;
    background: linear-gradient(135deg, rgba(248,250,252,0.1), rgba(15,23,42,0.2));
    cursor: pointer;
    transition: all 0.2s ease;
}

.nav-cta span {
    font-size: 0.8rem;
}

.nav-cta:hover {
    transform: translateY(-1px) translateX(1px);
    box-shadow: 0 10px 28px rgba(15,23,42,0.5);
    background: linear-gradient(135deg, rgba(248,250,252,0.2), rgba(15,23,42,0.5));
}

/* HERO (rw.html) */

.hero {
    flex: 1;
    display: grid;
    place-items: center;
    padding: 3rem 0 3.5rem;
}

.hero-inner {
    display: grid;
    grid-template-columns: minmax(0, 1.15fr) minmax(0, 0.9fr);
    gap: 2.5rem;
    align-items: center;
}

.eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.18rem 0.6rem;
    border-radius: 999px;
    background: rgba(15,23,42,0.85);
    color: #e5e7eb;
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.16em;
    margin-bottom: 1.1rem;
    box-shadow: 0 10px 25px rgba(15,23,42,0.5);
}

.eyebrow-dot {
    width: 9px;
    height: 9px;
    border-radius: 999px;
    background: radial-gradient(circle at 30% 0%, #facc15, #f97316);
}

.hero-title {
    font-size: clamp(2.2rem, 4vw, 3.2rem);
    line-height: 1.05;
    letter-spacing: -0.03em;
    margin-bottom: 1rem;
    color: #0f172a;
}

.hero-title span {
    background: linear-gradient(120deg, #f97316, #facc15, #f97316);
    -webkit-background-clip: text;
    color: transparent;
}

.hero-subtitle {
    max-width: 30rem;
    font-size: 0.98rem;
    color: #4b5563;
    line-height: 1.6;
    margin-bottom: 1.8rem;
}

.hero-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 1.2rem;
    align-items: center;
    margin-bottom: 2.1rem;
}

.badge {
    padding: 0.3rem 0.75rem;
    font-size: 0.75rem;
    border-radius: 999px;
    border: 1px solid rgba(15,23,42,0.1);
    background: rgba(255,255,255,0.75);
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    box-shadow: 0 12px 30px rgba(148,163,184,0.35);
}

.badge-pill {
    width: 8px;
    height: 8px;
    border-radius: 999px;
    background: radial-gradient(circle at 40% 0%, #22c55e, #166534);
}

.hero-time {
    font-size: 0.85rem;
    color: #374151;
    display: flex;
    align-items: center;
    gap: 0.45rem;
}

.dot {
    width: 4px;
    height: 4px;
    border-radius: 999px;
    background: #9ca3af;
}

.hero-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.9rem;
    align-items: center;
    margin-bottom: 2.5rem;
}

.btn-primary {
    padding: 0.75rem 1.4rem;
    border-radius: 999px;
    border: none;
    cursor: pointer;
    font-weight: 600;
    font-size: 0.95rem;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    background: radial-gradient(circle at 10% 0%, #f97316, #b91c1c);
    color: #f9fafb;
    box-shadow: 0 18px 40px rgba(148,27,12,0.7);
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    transition: transform 0.18s ease, box-shadow 0.18s ease;
}

.btn-primary:hover {
    transform: translateY(-2px) translateX(1px);
    box-shadow: 0 22px 65px rgba(148,27,12,0.9);
}

.btn-outline {
    padding: 0.7rem 1.3rem;
    border-radius: 999px;
    border: 1px solid rgba(15,23,42,0.18);
    font-size: 0.9rem;
    font-weight: 500;
    background: rgba(255,255,255,0.8);
    color: #111827;
    cursor: pointer;
    display: inline-flex;
    align-items: center;
    gap: 0.55rem;
    transition: all 0.2s ease;
}

.btn-outline:hover {
    background: rgba(15,23,42,0.95);
    color: #f9fafb;
    box-shadow: 0 15px 35px rgba(15,23,42,0.55);
    transform: translateY(-1px);
}

.hero-footnote {
    font-size: 0.8rem;
    color: #6b7280;
    display: flex;
    align-items: center;
    gap: 0.4rem;
}

.hero-footnote strong {
    color: #111827;
}

/* HERO IMAGE CARD */

.hero-card {
    position: relative;
    border-radius: 1.5rem;
    overflow: hidden;
    background: radial-gradient(circle at top left, #0f172a, #111827);
    color: #e5e7eb;
    padding: 1.5rem;
    min-height: 310px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 35px 75px rgba(15,23,42,0.85);
}

.hero-card-tag {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.18em;
    opacity: 0.85;
    margin-bottom: 0.6rem;
}

.hero-card-title {
    font-size: 1.45rem;
    line-height: 1.25;
    margin-bottom: 0.4rem;
}

.hero-card-title span {
    color: #facc15;
}

.hero-card-sub {
    font-size: 0.9rem;
    color: #9ca3af;
    max-width: 18rem;
    margin-bottom: 1.5rem;
}

.hero-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.75rem;
    margin-bottom: 1.4rem;
}

.mini-card {
    padding: 0.6rem 0.7rem;
    border-radius: 1rem;
    background: rgba(15,23,42,0.9);
    border: 1px solid rgba(148,163,184,0.5);
    font-size: 0.8rem;
    display: flex;
    flex-direction: column;
    gap: 0.15rem;
}

.mini-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    color: #9ca3af;
}

.mini-value {
    font-weight: 600;
    color: #fefce8;
}

.hero-bottom-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 0.75rem;
}

.chef {
    display: flex;
    align-items: center;
    gap: 0.6rem;
}

.chef-avatar {
    width: 38px;
    height: 38px;
    border-radius: 999px;
    border: 2px solid rgba(254,240,138,0.88);
    background: radial-gradient(circle at 20% 0%, #0f172a, #111827);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
}

.chef-text {
    font-size: 0.8rem;
}

.chef-text span {
    display: block;
    font-size: 0.7rem;
    color: #9ca3af;
}

.rating-pill {
    padding: 0.4rem 0.8rem;
    border-radius: 999px;
    background: rgba(15,23,42,0.95);
    border: 1px solid rgba(148,163,184,0.6);
    font-size: 0.75rem;
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
}

.spark {
    font-size: 0.8rem;
}

/* HOME PAGE SECTIONS */

.section {
    padding: 3rem 0 3.5rem;
}

.split {
    display: grid;
    grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
    gap: 2.25rem;
    align-items: start;
}

.section-label {
    font-size: 0.75rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #6b7280;
    margin-bottom: 0.75rem;
}

.section-title {
    font-size: clamp(1.6rem, 3vw, 2.1rem);
    letter-spacing: -0.03em;
    margin-bottom: 0.8rem;
    color: #111827;
}

.section-body {
    font-size: 0.95rem;
    color: #4b5563;
    line-height: 1.7;
    max-width: 32rem;
    margin-bottom: 1.4rem;
}

.pill-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 2rem;
}

.pill {
    padding: 0.35rem 0.8rem;
    font-size: 0.75rem;
    border-radius: 999px;
    border: 1px solid rgba(148,163,184,0.7);
    background: rgba(248,250,252,0.85);
}

.kpi-row {
    display: flex;
    flex-wrap: wrap;
    gap: 1.8rem;
    margin-top: 0.6rem;
}

.kpi {
    font-size: 0.85rem;
    color: #4b5563;
}

.kpi strong {
    display: block;
    font-size: 1.4rem;
    color: #111827;
}

.card-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.2rem;
}

.feature-card {
    border-radius: 1.25rem;
    padding: 1.1rem 1.1rem 1.2rem;
    background: rgba(255,255,255,0.85);
    border: 1px solid rgba(226,232,240,0.95);
    box-shadow: 0 14px 35px rgba(148,163,184,0.55);
    display: flex;
    flex-direction: column;
    gap: 0.45rem;
    position: relative;
    overflow: hidden;
}

.feature-tag {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.16em;
    color: #6b7280;
}

.feature-title {
    font-weight: 600;
    font-size: 0.95rem;
    color: #111827;
}

.feature-body {
    font-size: 0.82rem;
    color: #6b7280;
    line-height: 1.5;
}

.chip {
    align-self: flex-start;
    margin-top: 0.4rem;
    padding: 0.25rem 0.6rem;
    font-size: 0.7rem;
    border-radius: 999px;
    background: rgba(254,249,195,0.9);
    color: #854d0e;
}

/* MENU PAGE */

.menu-intro {
    text-align: center;
    margin-bottom: 2rem;
}

.menu-intro p {
    max-width: 32rem;
    margin: 0.75rem auto 0;
    font-size: 0.95rem;
    color: #4b5563;
}

.tabs {
    display: inline-flex;
    padding: 0.25rem;
    border-radius: 999px;
    background: rgba(15,23,42,0.06);
    border: 1px solid rgba(148,163,184,0.7);
    margin-bottom: 2rem;
}

.tab {
    padding: 0.45rem 1rem;
    border-radius: 999px;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    cursor: default;
    opacity: 0.75;
}

.tab.active {
    background: #0f172a;
    color: #f9fafb;
    opacity: 1;
}

.menu-grid {
    display: grid;
    gap: 1.3rem;
    grid-template-columns: repeat(3, minmax(0, 1fr));
}

.dish-card {
    border-radius: 1.2rem;
    padding: 0.95rem;
    background: rgba(255,255,255,0.9);
    border: 1px solid rgba(226,232,240,0.95);
    box-shadow: 0 13px 32px rgba(148,163,184,0.6);
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 0.7rem;
    align-items: center;
}

.dish-main h3 {
    font-size: 0.98rem;
    margin-bottom: 0.25rem;
    color: #111827;
}

.dish-meta {
    font-size: 0.8rem;
    color: #6b7280;
    margin-bottom: 0.4rem;
}

.badge-soft {
    display: inline-flex;
    padding: 0.15rem 0.55rem;
    border-radius: 999px;
    font-size: 0.7rem;
    background: rgba(22,163,74,0.08);
    color: #166534;
}

.price {
    margin-top: 0.4rem;
    font-weight: 600;
    color: #b91c1c;
    font-size: 0.92rem;
}

.dish-extra {
    font-size: 0.75rem;
    color: #6b7280;
    text-align: right;
}

.dot-row {
    display: flex;
    justify-content: flex-end;
    gap: 0.15rem;
    margin-bottom: 0.35rem;
}

.dot-row span {
    width: 4px;
    height: 4px;
    border-radius: 999px;
    background: rgba(148,163,184,0.9);
}

/* ADMIN PAGE */

.team-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.4rem;
}

.team-card {
    border-radius: 1.2rem;
    padding: 1rem 1.1rem 1.2rem;
    background: rgba(15,23,42,0.96);
    color: #e5e7eb;
    border: 1px solid rgba(148,163,184,0.85);
    box-shadow: 0 18px 50px rgba(15,23,42,0.9);
    display: flex;
    flex-direction: column;
    gap: 0.35rem;
}

.team-role {
    font-size: 0.75rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #9ca3af;
}

.team-name {
    font-size: 1.05rem;
    font-weight: 600;
}

.team-meta {
    font-size: 0.82rem;
    color: #d1d5db;
}

.shift {
    margin-top: 0.4rem;
    font-size: 0.78rem;
    color: #facc15;
}

/* CONTACT PAGE */

.contact-layout {
    display: grid;
    grid-template-columns: minmax(0, 1.05fr) minmax(0, 0.95fr);
    gap: 2rem;
}

.contact-card {
    border-radius: 1.3rem;
    padding: 1.4rem 1.5rem;
    background: rgba(255,255,255,0.9);
    border: 1px solid rgba(226,232,240,0.98);
    box-shadow: 0 22px 60px rgba(148,163,184,0.7);
}

.contact-card h2 {
    font-size: 1.5rem;
    margin-bottom: 0.4rem;
    color: #111827;
}

.contact-card p {
    font-size: 0.95rem;
    color: #4b5563;
    margin-bottom: 1.2rem;
}

.contact-item {
    margin-bottom: 1rem;
    font-size: 0.95rem;
}

.contact-item span {
    display: block;
    font-size: 0.78rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: #9ca3af;
    margin-bottom: 0.2rem;
}

.hours-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.4rem 1.2rem;
    font-size: 0.86rem;
    color: #4b5563;
}

.hours-grid span {
    font-weight: 500;
    color: #111827;
}

.form-card {
    border-radius: 1.3rem;
    padding: 1.4rem 1.5rem 1.7rem;
    background: rgba(15,23,42,0.96);
    color: #e5e7eb;
    border: 1px solid rgba(148,163,184,0.9);
    box-shadow: 0 24px 70px rgba(15,23,42,0.9);
}

.form-card h3 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

.form-card p {
    font-size: 0.85rem;
    color: #9ca3af;
    margin-bottom: 1.2rem;
}

.field {
    margin-bottom: 0.9rem;
}

.field label {
    display: block;
    font-size: 0.8rem;
    margin-bottom: 0.2rem;
    color: #e5e7eb;
}

.field input,
.field textarea {
    width: 100%;
    border-radius: 0.7rem;
    border: 1px solid rgba(148,163,184,0.8);
    padding: 0.55rem 0.65rem;
    font-size: 0.86rem;
    background: rgba(15,23,42,0.9);
    color: #e5e7eb;
    outline: none;
}

.field textarea {
    min-height: 80px;
    resize: vertical;
}

.field input:focus,
.field textarea:focus {
    border-color: #f97316;
    box-shadow: 0 0 0 1px rgba(248, 113, 22, 0.4);
}

.form-note {
    font-size: 0.75rem;
    color: #9ca3af;
    margin-top: 0.5rem;
}

.submit-btn {
    margin-top: 0.3rem;
    padding: 0.65rem 1.2rem;
    border-radius: 999px;
    border: none;
    cursor: pointer;
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    background: radial-gradient(circle at 10% 0%, #f97316, #b91c1c);
    color: #f9fafb;
    box-shadow: 0 15px 40px rgba(148,27,12,0.8);
    transition: transform 0.18s ease, box-shadow 0.18s ease;
}

.submit-btn:hover {
    transform: translateY(-1px);
    box-shadow: 0 20px 60px rgba(148,27,12,0.9);
}

/* FOOTER */

.footer {
    border-top: 1px solid rgba(148,163,184,0.4);
    padding: 1rem 0;
    margin-top: auto;
    backdrop-filter: blur(10px);
    background: rgba(248,250,252,0.8);
}

.footer-inner {
    font-size: 0.78rem;
    color: #6b7280;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 0.75rem;
    flex-wrap: wrap;
}

.footer-inner span strong {
    color: #111827;
}

.footer-links {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
}

.footer-links a {
    text-decoration: underline;
    text-decoration-style: dotted;
    text-underline-offset: 2px;
}

/* RESPONSIVE */

@media (max-width: 900px) {
    .hero-inner,
    .split,
    .contact-layout {
        grid-template-columns: minmax(0, 1fr);
    }

    .hero {
        padding-top: 2.4rem;
    }

    .hero-card {
        order: -1;
    }

    .hero-title {
        font-size: clamp(1.9rem, 7vw, 2.3rem);
    }

    .card-grid,
    .menu-grid,
    .team-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .dish-card {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 640px) {
    .nav-inner {
        flex-wrap: wrap;
        justify-content: center;
    }

    .nav-links {
        justify-content: center;
        flex-wrap: wrap;
    }

    .hero-actions {
        flex-direction: column;
        align-items: flex-start;
    }

    .card-grid,
    .menu-grid,
    .team-grid {
        grid-template-columns: minmax(0, 1fr);
    }

    .container {
        padding-inline: 1.1rem;
    }
}

```

## OUTPUT:
<img width="1880" height="1193" alt="image" src="https://github.com/user-attachments/assets/547bab59-4ed7-4ab2-84a0-e750ba7c4e7a" />
![Uploading image.png…]()
<img width="1884" height="1199" alt="Screenshot 2025-11-22 105956" src="https://github.com/user-attachments/assets/bcb48fb2-4a24-45d3-873a-4ae9ec3561a0" />
<img width="1888" height="1199" alt="Screenshot 2025-11-22 110017" src="https://github.com/user-attachments/assets/aa06261e-17de-4f43-987f-dc805557fa1a" />


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
