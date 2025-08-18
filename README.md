[![Releases](https://img.shields.io/badge/Releases-Download-blue?logo=github&style=for-the-badge)](https://github.com/Xggs369/JovenesAProgramar25/releases)

# Track Programa 2025: Coding Progress, Projects, and Labs Hub

![Hero image](https://images.unsplash.com/photo-1522199755839-a2bacb67c546?auto=format&fit=crop&w=1400&q=80)

Table of contents
- Overview 🚀
- How to get the release and run it ⬇️
- Quick start — run locally 🖥️
- Prerequisites and tools 🧰
- Project layout 📁
- Workflows and scripts ⚙️
- HTML / CSS / JS examples 🧩
- Learning log — progress diary 📓
- Weekly plan and milestones 🗓️
- How I test code ✅
- Debug tips and common fixes 🐞
- Design system and assets 🎨
- Deployment guide 🌐
- Contribute and pull request guide 🤝
- Roadmap and next steps 🔭
- Resources and links 🔗
- FAQ ❓
- License and contact ✉️

Overview 🚀
This repository stores my progress in a web development course for 2025. I use it as a lab. I build pages, components, small scripts, and demos. I record notes and code. I track tasks and tasks done. I keep release builds in the Releases page. Use the badge above or visit the Releases area to fetch builds.

How to get the release and run it ⬇️
- Visit the releases page and download the most recent build:
  https://github.com/Xggs369/JovenesAProgramar25/releases
- Download the packaged file for the release. The release contains one or more assets.
- After download, run the included file or script that matches your platform.
  - If it is a ZIP file, extract it and run index.html to open the demo.
  - If it is a .tar.gz, extract and open the demo files.
  - If it is a script (.sh or .bat), mark it executable and run it.
- The releases page may include a readme for the release. Follow that readme for exact steps.

Quick start — run locally 🖥️
1. Clone the repo:
   git clone https://github.com/Xggs369/JovenesAProgramar25.git
2. Open the project folder:
   cd JovenesAProgramar25
3. Serve the site:
   - Use a simple static server:
     npx http-server -c-1 ./public
   - Or open public/index.html in your browser.
4. View examples in the samples/ folder.
5. To run the interactive demos, open the corresponding HTML file.

Prerequisites and tools 🧰
- Git — for version control.
- Node.js — for tooling and local servers.
- npm or yarn — to install dev tools.
- A modern browser (Chrome, Firefox, Edge, or Safari).
- Code editor (VS Code, Atom, or Sublime).
- Optional: Live Server extension for quick view.

Install recommended dev tools
- Install Node.js LTS.
- Install http-server for quick serve:
  npm install -g http-server
- Install Prettier for stable formatting:
  npm install --save-dev prettier
- Install ESLint for linting:
  npm install --save-dev eslint

Project layout 📁
This repo follows a clear layout. Each folder maps to a topic or exercise. Keep changes in your own branch. Use PRs to merge changes to main.

Root
- README.md — this document.
- CONTRIBUTING.md — contribution rules.
- LICENSE — license file.
- package.json — scripts and dev deps.
- public/ — production-ready static files.
- src/ — source code for exercises.
- samples/ — demo pages and small projects.
- assets/ — images, icons, and fonts.
- docs/ — notes, guides, and study material.
- logs/ — weekly logs and progress notes.

public/
- index.html — main demo entry.
- css/ — compiled styles.
- js/ — compiled scripts.
- img/ — exported images.

src/
- css/ — SCSS or modular CSS.
- js/ — raw JavaScript modules.
- components/ — small UI components.
- pages/ — page templates.

samples/
- session-01/ — HTML basics.
- session-02/ — CSS layout exercises.
- session-03/ — JavaScript DOM tasks.
- ui-kit/ — buttons, forms, and cards.

Workflows and scripts ⚙️
Use package.json scripts to standardize tasks. Here are common commands:

- npm run serve
  - Start a local static server and watch files.
- npm run build
  - Compile and minify CSS and JS to public/.
- npm run lint
  - Run ESLint on src/.
- npm run format
  - Run Prettier on the repo.

Example package.json scripts
```json
{
  "scripts": {
    "serve": "http-server ./public -p 8080 -c-1",
    "build": "npm run build:css && npm run build:js",
    "build:css": "sass src/css:public/css --no-source-map --style=expanded",
    "build:js": "rollup -c",
    "lint": "eslint src --ext .js,.jsx",
    "format": "prettier --write \"**/*.{js,css,html,md}\""
  }
}
```

HTML / CSS / JS examples 🧩
The samples folder holds small, focused demos. Copy code into your projects. Test in modern browsers.

Simple responsive layout (HTML)
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Grid Demo</title>
  <link rel="stylesheet" href="../public/css/grid.css" />
</head>
<body>
  <header class="site-header">
    <h1>Grid Demo</h1>
  </header>
  <main class="grid">
    <article class="card">Card 1</article>
    <article class="card">Card 2</article>
    <article class="card">Card 3</article>
    <article class="card">Card 4</article>
  </main>
  <footer class="site-footer">2025 Lab</footer>
</body>
</html>
```

Simple CSS snippet (CSS Grid)
```css
.grid {
  display: grid;
  gap: 12px;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  padding: 16px;
}
.card {
  background: #fff;
  border-radius: 8px;
  padding: 18px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.06);
}
```

Vanilla JS: small DOM widget
```js
// Toggle a class on click
document.addEventListener('click', function (e) {
  var btn = e.target.closest('[data-toggle]');
  if (!btn) return;
  var target = document.querySelector(btn.getAttribute('data-toggle'));
  if (target) target.classList.toggle('is-open');
});
```

Learning log — progress diary 📓
This section holds my study notes, task lists, and reflections. I write a short entry after each session. Each entry lists the goals, the steps I took, and the results. I keep entries short and factual.

Example log entry
- Date: 2025-03-12
- Theme: HTML5 forms
- Goal: Build a form with validation that posts to a mock API.
- Work: Created form markup. Added basic CSS. Wrote validation script using Constraint Validation API. Tested with JSONPlaceholder.
- Result: Form submits and shows a success message. Logged errors to console. Added unit tests for validation functions.

I track time per task and mark priority. I label tasks as "learn", "practice", or "deliver". I push code at the end of the day. This gives a clear snapshot of progress.

Weekly plan and milestones 🗓️
I plan work by week. Each week has a focus. The list below shows a sample 12-week plan.

Week 1 — HTML structure, semantic tags, forms.
Week 2 — CSS basics, box model, layout with Flexbox.
Week 3 — CSS Grid and responsive design.
Week 4 — JavaScript fundamentals: types, arrays, functions.
Week 5 — DOM manipulation and events.
Week 6 — Fetch API and async patterns.
Week 7 — Build a small SPA with vanilla JS.
Week 8 — CSS architecture, variables, and themes.
Week 9 — Accessibility basics and ARIA.
Week 10 — Testing small units and UI.
Week 11 — Optimization and performance basics.
Week 12 — Final mini-project and showcase.

Each week has deliverables. I tag each deliverable and link to commits and releases. I use the Releases area for milestone builds. Check the releases page for packaged milestones:
https://github.com/Xggs369/JovenesAProgramar25/releases

How I test code ✅
I run small tests and snapshot checks. I prefer manual tests for UI. I automate logic tests with Jest or simple assertions.

Sample test for a validation function
```js
function isEmail(val) {
  return /\S+@\S+\.\S+/.test(val);
}

console.assert(isEmail('test@example.com') === true, 'valid email');
console.assert(isEmail('bad-email') === false, 'invalid email');
```

UI testing
- Open the page in a browser.
- Trigger the interaction.
- Observe the DOM and the network panel.
- Check console for errors.

Debug tips and common fixes 🐞
- If CSS does not apply, check selector specificity.
- If JS fails, open DevTools Console and inspect the stack trace.
- If an import fails, check file paths and names.
- If a build step fails, run it in verbose mode to see the error.
- For cross-origin issues, use a local server instead of file://.
- If images do not load, check the case of filenames and image path.

Design system and assets 🎨
I keep a small design system. It includes colors, spacing scale, typography tokens, and basic components such as buttons and forms. I use simple naming. I store the tokens in CSS variables to keep them easy to update.

Design tokens (CSS variables)
```css
:root {
  --color-bg: #f6f8fb;
  --color-card: #ffffff;
  --color-primary: #0078d4;
  --color-accent: #1fa2ff;
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 16px;
  --space-4: 24px;
  --radius-1: 6px;
  --radius-2: 12px;
}
```

Guidelines
- Use the scale for spacing.
- Use tokens for colors and fonts.
- Keep components small and composable.
- Write styles that degrade well on older browsers.

Assets
- Icons: use simple SVG icons in /assets/icons/.
- Images: use compressed JPEG or WebP in /assets/img/.
- Fonts: use system fonts or load a single web font to reduce weight.

Deployment guide 🌐
I deploy static builds to GitHub Pages or other static hosts. I keep deploy steps short.

Deploy steps (GitHub Pages)
1. Build the site:
   npm run build
2. Push public/ to gh-pages branch:
   npm run deploy
3. Verify site on https://username.github.io/repo-name

Deploy steps (Netlify)
1. Connect repository to Netlify.
2. Set build command: npm run build
3. Set publish directory: public
4. Trigger deploy.

CI tips
- Run lint and tests in CI.
- Use a small Docker image for consistency.
- Cache node_modules to speed up builds.

Contribute and pull request guide 🤝
I accept contributions. Follow this process.

1. Fork the repository.
2. Create a branch for your change:
   git checkout -b feature/clear-layout
3. Make small, focused commits.
4. Run lint and format before pushing.
5. Open a Pull Request describing your change.
6. Use clear commit messages. Use present tense.
7. Link to issues if relevant.

Pull request checklist
- The code builds.
- Tests pass.
- The change is documented.
- The change follows the component and style guidelines.

Code of conduct
Be kind and be respectful. Keep discussions about the code. Focus on facts. Use clear language.

Roadmap and next steps 🔭
The roadmap lists features and study goals. I break features into small tasks and track them in issues.

Planned items
- Add a small, interactive learning game using JS.
- Build a CSS component library and document it.
- Add an accessibility audit and fixes.
- Add integration tests for key pages.
- Add more sample projects and code challenges.

Milestones
- M1: HTML and CSS core topics complete.
- M2: JavaScript fundamentals complete.
- M3: Mini-project delivered and packaged.
- M4: Portfolio-ready build.

Resources and links 🔗
I link to guides, docs, and helpful tools. Use them to learn the same topics.

Learning references
- MDN Web Docs — HTML, CSS, JS guides.
- CSS-Tricks — layout and patterns.
- freeCodeCamp — exercises and tutorials.
- HTML5 Rocks — compatibility and features.
- JavaScript.info — deep dive into JS.

Tools and utilities
- Prettier — code formatting.
- ESLint — linting rules.
- Rollup or Webpack — bundling.
- Browsersync or http-server — local serve.

Images and icons used
- Hero image from Unsplash: https://images.unsplash.com/photo-1522199755839-a2bacb67c546
- Icon set: use free SVG icons from public icon sets.

FAQ ❓
Q: How do I run a demo?
A: Clone the repo, run npm install if needed, then serve the public/ folder.

Q: How do I add a new sample?
A: Create a folder in samples/ with a descriptive name. Add index.html, css, and js. Add a short README.md that explains the goal.

Q: How do I request a feature?
A: Open an issue and describe the feature. Mark it as "feature-request". Add a short use case and a mock if you can.

Q: How do I build for production?
A: Run npm run build. The compiled files will appear in public/. Use a static host to serve them.

Q: Where are the release builds?
A: Look in the Releases section on GitHub:
https://github.com/Xggs369/JovenesAProgramar25/releases
Download the appropriate asset and run the included file or script.

Code style and patterns
I follow a small set of rules to keep the code consistent.

- Use short functions that do one job.
- Prefer const and let over var.
- Use module imports and exports.
- Keep CSS modular and use BEM or simple class names.
- Keep components small and composable.

JS example: module pattern
```js
// utils/math.js
export function clamp(value, min, max) {
  return Math.max(min, Math.min(max, value));
}
```

CSS naming example
- base/
  - .site-header
  - .site-footer
- components/
  - .btn
  - .card
- util/
  - .u-hidden
  - .u-clearfix

Testing and CI
I run unit tests for pure functions. I use basic end-to-end checks for UI flows.

Test framework
- Jest for unit tests.
- Puppeteer for simple UI checks.
- Lighthouse for performance and accessibility audits.

Sample Jest test
```js
import { clamp } from '../src/js/utils/math';

test('clamp within range', () => {
  expect(clamp(5, 1, 10)).toBe(5);
});

test('clamp below min', () => {
  expect(clamp(-1, 0, 5)).toBe(0);
});
```

Common Git workflow
- Main branch holds stable work.
- Create a feature branch for each change.
- Rebase or merge main before final PR.
- Use small commits and clear messages.

Branch naming
- feature/feature-name
- fix/issue-number
- chore/tool-update

Screenshots and demos 📷
Below are sample screenshots and demo links. Use them to preview finished work.

Demo screenshot
![Demo screenshot](https://images.unsplash.com/photo-1515879218367-8466d910aaa4?auto=format&fit=crop&w=1200&q=80)

Card component screenshot
![Card screenshot](https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1200&q=80)

Sample demo link
- Open public/index.html after build to view a demo.

Template snippets and starter kits
I keep a few starter templates here for quick practice.

Starter: Minimal HTML
- index.html
- css/reset.css
- css/styles.css
- js/main.js

Starter: Component kit
- components/button.html
- components/form.html
- components/modal.html

Accessibility checklist
- Provide semantic HTML.
- Use labels for form controls.
- Ensure keyboard navigation.
- Provide alt text for meaningful images.
- Maintain a logical heading order.
- Ensure sufficient color contrast.

Performance checklist
- Minify CSS and JS in production.
- Use compressed images.
- Use lazy loading for images.
- Reduce the number of third-party scripts.
- Use HTTP caching where possible.

Study exercises and tasks
I include many practice tasks. Each task includes a goal and a test.

Task 1 — Build a responsive card
- Goal: Create a card with title, image, and footer. It must be responsive.
- Test: The card must display at one column on narrow screens and three columns on wide screens.

Task 2 — Form validation
- Goal: Build a form that validates email and password.
- Test: The submit button must be disabled until validation passes.

Task 3 — Small SPA routing
- Goal: Build a single-page structure with dynamic content swapping.
- Test: The page must change content with no full reload.

Week-by-week sample entries (expanded)
I keep many entries. I record what I learned and what I will do next. Below are extended entries that show my workflow.

Week 1 — Day by day
- Day 1: Set up repo. Create folders. Add readme. Create a simple index.html.
- Day 2: Study semantic tags. Replace divs with header, main, footer. Test in browser.
- Day 3: Build a form. Add labels and input elements. Add basic CSS.
- Day 4: Add simple validation script using HTML5 validation. Test error messages.
- Day 5: Polish styles. Add a little JS to focus the first field. Commit and push.

Week 2 — CSS and layout
- Day 1: Learn Flexbox. Create a responsive navigation.
- Day 2: Create a grid demo with images. Use object-fit for images.
- Day 3: Learn media queries. Adjust typography at breakpoints.
- Day 4: Add CSS variables for colors and spacing.
- Day 5: Document the style tokens in docs/design.md.

Week 3 — JS basics and DOM
- Day 1: Learn let and const. Practice with small snippets.
- Day 2: Work with arrays and map/filter/reduce.
- Day 3: Manipulate the DOM: add and remove elements.
- Day 4: Build a small todo list that persists to localStorage.
- Day 5: Add tests for utility functions.

Code snippets and patterns (reference)
Event delegation
```js
document.querySelector('#list').addEventListener('click', function (e) {
  var item = e.target.closest('.item');
  if (!item) return;
  // handle item click
});
```

Fetch with error handling
```js
async function fetchJson(url) {
  const res = await fetch(url);
  if (!res.ok) throw new Error('Network error');
  return res.json();
}
```

LocalStorage helper
```js
export function save(key, value) {
  localStorage.setItem(key, JSON.stringify(value));
}
export function load(key) {
  const raw = localStorage.getItem(key);
  return raw ? JSON.parse(raw) : null;
}
```

Common pitfalls and how I fix them
- Mixed content: use https for all resources.
- CORS: use the correct headers on API or proxy calls.
- Relative paths: test both from root and from nested routes.

Automation and reproducibility
I aim to make builds reproducible. I pin specific versions in package.json. I save build artifacts in the Releases area for key milestones. Releases hold zip files, example data, and short instructions.

Release packaging checklist
- Include the built public/ folder.
- Include a README for the release with exact steps.
- Include sample data used by the demo.
- Include a changelog.txt listing important changes.

Changelog format
- v0.1.0 — Initial HTML and CSS samples.
- v0.2.0 — Added JavaScript exercises and todo app.
- v0.3.0 — Added small SPA demo and routing example.

Security notes
- Keep secrets out of the repo.
- Use environment variables for any API keys in builds.
- Avoid committing .env and similar files.

Contact and feedback ✉️
I accept issues and pull requests. Use GitHub issues for bugs and feature requests. Use PR comments for design and code reviews.

Acknowledgements and credits
- This repo uses free images from Unsplash.
- Icons come from public icon sets.
- Tutorials and references list credit to MDN and community guides.

Badges and status
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=flat-square)](https://github.com/Xggs369/JovenesAProgramar25/actions)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)

Local environment example
- Node 18.x
- npm 9.x
- macOS, Linux, or Windows Subsystem for Linux

Sample branch and release strategy
- main: stable code.
- dev: active changes.
- feature/*: for features.
- Use Releases for milestone artifacts and package builds.

More reading and study tasks
- Build a small accessible widget each week.
- Read a chapter from MDN on a weekly topic.
- Recreate a small UI from a design sample and explain choices.

Appendix — small utilities and snippets
Keyboard helper
```js
function onEnter(event, cb) {
  if (event.key === 'Enter') cb();
}
```

Throttle helper
```js
export function throttle(fn, wait = 200) {
  let last = 0;
  return function(...args) {
    const now = Date.now();
    if (now - last >= wait) {
      last = now;
      fn.apply(this, args);
    }
  };
}
```

SVG icon usage
```html
<svg class="icon" width="24" height="24" aria-hidden="true">
  <use xlink:href="#icon-search"></use>
</svg>
```

Final notes on using releases
- The releases page holds downloadable build artifacts.
- Download the file that matches your environment.
- Run the included script or open index.html to view demos.
- The releases page link appears earlier and here again:
  https://github.com/Xggs369/JovenesAProgramar25/releases

License and legal ✍️
All code in this repository uses the MIT License unless noted. You can use the code for study and personal projects. See the LICENSE file for full terms.

Contact
- Open an issue for questions.
- Create a pull request to share improvements.
- Use the GitHub profile for direct contact.

Thank you for checking this workspace.