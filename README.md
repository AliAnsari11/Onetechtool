# ONETECH website

Static website (HTML, CSS, JavaScript). Koi build step ya framework nahi chahiye.

## Structure

```
onetech-site/
├── index.html            Home
├── projects.html         Saare projects
├── item.html             Product / project detail (?type=product&slug=...)
├── contact.html          Contact form
├── privacy-policy.html
├── terms-of-use.html
├── cookie-policy.html
├── css/style.css         Saari styling
├── js/
│   ├── data.js           Saara content (products, projects, news, contact info)
│   └── main.js           Header, footer aur sections render karta hai
└── assets/
    ├── images/           Images yahan rakhein
    └── catalogs/         PDF catalogs yahan rakhein
```

## Local chalana
```
python3 -m http.server 8000   # phir http://localhost:8000
```

## GitHub Pages par deploy
1. Repo push karein.
2. Settings → Pages → Source: `main` branch, `/ (root)`.
3. Custom domain ke liye Pages settings mein `onetech-tools.com` add karein.

## Baaki kaam (TODO)
- Images aur PDFs abhi purani site ke CDN se load ho rahe hain. Unhe download karke `assets/` mein rakhein aur `js/data.js` ke paths badlein, kyunki purani site band hone par woh links toot jayenge.
- `contact.html` mein `YOUR_FORM_ID` ko apne Formspree form ID se badlein.
- Legal pages ka asli text paste karein.
- Product aur project ka poora description `js/data.js` mein add karein.
