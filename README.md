# Sleek Dynamic Pricing App 💎

A high-performance, responsive pricing table component designed with modern UI/UX principles. This project demonstrates a transition from static "spaghetti" code to a modular, data-driven architecture.

## 🌟 Features

- **Live Currency Conversion**: Integrates with the [Frankfurter API](https://www.frankfurter.dev/) to fetch real-time exchange rates for USD, EUR, GBP, and JPY.
- **Dynamic Billing Logic**: Toggle between monthly and yearly billing with an automatic 20% discount calculation.
- **Dark Mode Support**: Includes a theme-switcher with user preference persistence via `localStorage`.
- **Responsive & Sleek UI**: Built using CSS Grid and Glassmorphism effects. Fully responsive from mobile to ultra-wide displays.
- **Semantic & Accessible**: Uses HTML5 tags (`<main>`, `<section>`, `<label>`) for better SEO and screen-reader support.

## 🛠️ Tech Stack

- **HTML5**: Semantic structure.
- **CSS3**: Custom properties (variables), Grid, Flexbox, and Glassmorphism.
- **JavaScript (ES6+)**: Async/Await for API calls, DOM manipulation, and state management.

## 🚀 How It Works

### Data-Driven Rendering

The app separates content from logic. Pricing plans are stored in a JavaScript object, allowing for easy updates without touching the HTML structure.

### Live Exchange Rates

The app uses the `Intl.NumberFormat` API to ensure that currency symbols and decimal places are formatted correctly according to international standards.

````javascript
// Example of the live conversion logic
let price = isYearly ? (plan.usd * 0.8) : plan.usd;
let convertedPrice = (price * rates[currency]).toLocaleString(undefined, {
  style: 'currency',
  currency: currency
});


### 📦Installation & Usage

1. **Clone the repository:**

   ```bash
   git clone https://github.com/oluwafemi00/Pricing-project.git
```


2. **Open the project:**
   Simply open index.html in any modern web browser. No build steps or dependencies required!

### Refactor Journey

This project evolved through several distinct stages of software maturation:

- V1: Basic Flexbox layout with hardcoded values
  - Initial proof of concept focused on basic layout.

- V2: Introduction of CSS Variables and Semantic HTML
  - Refactored for maintainability and accessibility (a11y).

- V3: Data-driven rendering to eliminate "DRY" code smells
  - Moved content into JavaScript objects to automate HTML generation.

- V4: Implementation of API integration and Dark Mode
  - Added real-world functionality with live currency rates and user theme persistence.
````
