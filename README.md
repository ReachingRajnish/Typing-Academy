# Kids Typing Academy 🦁🎓

A premium, engaging, and calming touch-typing tutor and game designed specifically for kids. The application is built as an E2E frontend prototype that works seamlessly on both laptop physical keyboards and iPad touch screens.

## 🌟 Features

### 1. Typing School (Practice Mode) 🏫
* **20 Progressive Lessons**: Structured, progressive touch-typing lessons covering the Home Row, Top Row, Bottom Row, Short Words, and Full Sentences.
* **Real-time Statistics**: Live speed tracking in **WPM** (Words Per Minute), **Accuracy** (🎯 percentage), and mistake count (❌).
* **Hand Placement Guide**: An animated hand placement instruction screen displaying visual color-coded home row keys along with a CSS slide-in animation of human hand outlines. Includes a skip guide toggle stored in browser memory.
* **Mastery Progression**: Custom threshold requirements (Speed: 10/15/20 WPM, Accuracy: 90%) to automatically unlock the next lesson.
* **Interactive Feedback Banner**: Shows supportive tips when repeating a lesson. Clicking anywhere immediately skips back to practice, while clicking on the banner itself extends the reading time to 14 seconds.
* **Pulsing Key Highlights**: Active keys pulse dynamically with touch-typing color codes, keeping the visual layout clean and clutter-free.

### 2. Safari Game (Play Mode) 🌍
* **Rich Vocabulary**: A dictionary of over 500 words categorized by difficulty (3 to 7+ letters) including animals, colors, and verbs.
* **Reacting Emojis**: Gamified emoji animals that respond to typing performance (happy bounce for correct words, shaking gray outline for typos).
* **Score System**: Reward points based on word length and typing accuracy.

### 3. Hybrid Input System ⌨️📱
* **Physical Keyboards**: Fully optimized keydown event listeners for laptops and desktops.
* **Virtual Keyboards**: Apple Magic Keyboard-inspired responsive interface that listens to pointer events for tablet/iPad users.

---

## 🛠️ Technical Stack & Architecture

The application is structured as a self-contained, lightweight, single-page web app.

* **Core**: HTML5, CSS3, Vanilla JavaScript (ES6).
* **Styling**: Tailwind CSS (via CDN) for rapid layout grid development, paired with custom CSS for 3D buttons, custom scrollbars, and animations.
* **Audio Engine**: **Tone.js** (PolySynth combined with Reverb and Chorus effects). Correct inputs play keys stepping through a pentatonic scale (C, D, E, G, A), translating typing speed and rhythm into procedural melodies.
* **Typography**: *Fredoka One* (playful headers) and *Nunito* (highly readable UI font, buttons, and custom dropdown items) loaded via Google Fonts.

---

## 🎨 Design Philosophy

* **Apple-Style Aesthetics**: Clean grid layout with smooth, premium shadows to represent a high-end physical keyboard.
* **Calming Learning Environment**: Avoids harsh buzzers or annoying error sounds, replacing them with a procedural "Kalimba/Wind Chime" scale to ensure key errors are soft, while correct typing creates pleasant music.
* **Color-Coded Touch Zones**: Consistent color schemes mapping fingers to specific keyboard columns (Pinkies = Pink, Rings = Blue, Middles = Green, Index = Orange/Purple, Thumbs = Slate).
* **Perfect Alignment**: Dropdown menu is absolutely centered in the header and styled identically to the menu controls to prevent text wrapping.

---

## 🚀 Getting Started

Since the application is built entirely as a standalone frontend prototype, there are no heavy server setups or databases required.

### Run Locally
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/ReachingRajnish/Typing-Academy.git
   ```
2. Open `index.html` directly in your web browser, or use a local development server (such as Live Server in VS Code, or python's built-in server):
   ```bash
   python -m http.server 8000
   ```
3. Navigate to `http://localhost:8000/index.html` in your browser.