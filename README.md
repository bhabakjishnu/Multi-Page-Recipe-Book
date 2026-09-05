# 🚀 MULTI-PAGE-RECIPE-BOOK

A static, multi-page HTML and CSS web application showcasing various culinary recipes.

## 📖 Project Overview

The MULTI-PAGE-RECIPE-BOOK is a frontend web project that provides a digital collection of food recipes organized into individual static pages. It relies strictly on core web technologies to deliver a structured, easily navigable cookbook experience. The project emphasizes clean directory organization and a highly modular approach to CSS design.

## 🔗 Demo

Live Demo: [LIVE_DEMO_URL]

## ✨ Features

* **Multi-Page Routing**: Includes dedicated HTML pages for multiple distinct recipes, specifically Butter Naan, Chicken, Fried Rice, Khichuri, Mutton, and Sabji Vat.
* **Modular CSS Architecture**: Styles are logically separated into distinct files including `reset.css`, `tokens.css`, `layout.css`, `components.css`, `style.css`, and `recipe-detail.css` for maintainability and scalability.
* **Clean Asset Management**: Images and HTML pages are categorized securely into dedicated subdirectories within the central `assets` folder.
* **Zero Dependencies**: Built entirely with vanilla HTML and CSS, requiring no build tools, frameworks, or package managers.

## 📸 Project Preview

## 💻 Tech Stack

| Technology | Purpose |
| --- | --- |
| **HTML5** | Core content structure and multi-page linking |
| **CSS3** | Layout styling, component design, and responsive behaviors |

## 📂 Project Structure

The repository follows a clean, logical file structure utilizing relative paths:

```text
MULTI-PAGE-RECIPE-BOOK/
│
├── assets/
│   ├── css/
│   │   ├── components.css
│   │   ├── layout.css
│   │   ├── recipe-detail.css
│   │   ├── reset.css
│   │   ├── style.css
│   │   └── tokens.css
│   ├── images/
│   │   └── recipes/
│   │       ├── Butternaan.jpg
│   │       ├── Chicken.jpg
│   │       ├── Friedrice.jpg
│   │       ├── images1.jpg
│   │       ├── images2.jpg
│   │       ├── images3.png
│   │       ├── Khichuri.jpg
│   │       ├── Mutton.jpg
│   │       └── Sabjivat.jpg
│   └── pages/
│       ├── Butternaan.html
│       ├── Chicken.html
│       ├── Friedrice.html
│       ├── Khichuri.html
│       ├── Mutton.html
│       └── Sabjivat.html
│
└── index.html

```

## 🚀 Installation

To view or modify this project locally, follow these steps:

1. Clone the repository:
```bash
git clone [REPOSITORY_URL]

```


2. Navigate to the project directory:
```bash
cd MULTI-PAGE-RECIPE-BOOK

```



## 🖱️ Usage

Because this is a static website, no development server or environment configuration is required.
Simply double-click the `index.html` file in the root directory to open it in your default web browser. From there, you can navigate through the recipe links.

## ⚙️ How It Works

1. **Entry Point**: The user opens the root `index.html` file.
2. **Navigation**: The index page acts as the main directory, providing links to individual HTML files located in the `assets/pages/` directory.
3. **Rendering**: As the user navigates, each page pulls in global stylesheets (like `reset.css` and `tokens.css`) and specific stylesheets (like `recipe-detail.css`) from the `assets/css/` directory to render the UI.

## 🧠 Key Concepts & Learning Outcomes

* **Semantic HTML**: Structuring content appropriately across multiple distinct web pages.
* **CSS Organization**: Utilizing design tokens (`tokens.css`), resets (`reset.css`), layout structures (`layout.css`), and localized styling (`recipe-detail.css`) for a professional, scalable CSS architecture.
* **Relative Pathing**: Managing anchor links and image `src` paths seamlessly between sibling and nested directories.

## 📱 Responsive Design

This project utilizes standard CSS practices for cross-device compatibility:

* Fluid layout techniques targeting mobile, tablet, and desktop viewports.
* Media queries adjusting grid/flex structures based on screen width.

## ♿ Accessibility

* Semantic HTML5 tags ensure baseline screen-reader support.

## 🌐 Browser Compatibility

Tested and compatible with modern web browsers:

* Google Chrome
* Mozilla Firefox
* Microsoft Edge
* Apple Safari

## ⚡ Performance

* The separation of CSS concerns (tokens, layout, components) prevents monolithic, render-blocking stylesheets.
* Pure static file architecture ensures instantaneous loading times with zero server-side latency.

## 🧪 Testing

There is no automated testing framework currently implemented for this static HTML/CSS project.

## 🐛 Known Issues

No known issues at this time.

## 🔮 Future Improvements

* **Dark Mode**: Implement a theme toggle utilizing custom CSS properties/variables.
* **JavaScript Interactivity**: Add client-side filtering or a search bar for quick recipe discovery.
* **Dynamic Data Integration**: Refactor the static HTML pages to pull JSON recipe data dynamically via a modern frontend framework.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository.
2. Clone your fork: `git clone [YOUR_FORK_URL]`
3. Create a feature branch: `git checkout -b feature/amazing-feature`
4. Commit your changes: `git commit -m 'feat: add amazing feature'`
5. Push to the branch: `git push origin feature/amazing-feature`
6. Open a Pull Request.

### Commit Convention

* `feat:` — New feature
* `fix:` — Bug fix
* `docs:` — Documentation adjustments
* `style:` — CSS/Styling improvements
* `refactor:` — Code refactoring without changing functionality

## 📜 License

This project is licensed under the [LICENSE].

## 👤 Author

**[AUTHOR_NAME]**

* GitHub: [@GITHUB_USERNAME](https://www.google.com/search?q=https://github.com/%5BGITHUB_USERNAME%5D)
* LinkedIn: [LINKEDIN_PROFILE]
* Portfolio: [PORTFOLIO_URL]

## 📞 Contact

If you have any questions or feedback, feel free to reach out via [CONTACT_METHOD].

## ⭐️ Support

If you found this project helpful or inspiring, please consider giving it a ⭐️ on GitHub!