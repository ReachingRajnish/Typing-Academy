Project Memory: Kids Typing Academy

1. Project Overview

Name: Kids Typing Academy
Platform: Web Application (Responsive: optimized for both laptop physical keyboards and iPad touch screens).
Goal: A premium, engaging, and calming touch-typing tutor and game designed specifically for kids.
Development Phase: E2E Frontend Prototype (V2 completed - custom dropdown styling, hand placement instruction screen, dynamic click-to-dismiss feedback banner, and clean spacebar integration).

2. Tech Stack & Architecture

The current prototype is a self-contained, single-file frontend application.

Core: HTML5, CSS3, Vanilla JavaScript (ES6).

Styling: Tailwind CSS (via CDN) for rapid, responsive layout. Custom CSS for specific 3D button effects, custom scrollbars, animations, and typography.

Audio Engine: Tone.js (PolySynth with Reverb and Chorus) for generating procedural, calming musical feedback.

Fonts: 'Fredoka One' (playful headers) and 'Nunito' (readable UI text, buttons, and dropdown options) via Google Fonts.

3. Core Features & Modes

Safari Game (Play Mode):

- A 500+ word dictionary (animals, colors, action verbs, 3 to 7+ letters).
- Gamification via Emoji animals that react to the user (happy bounce for completion, grayscale shake for typos).
- Score tracking.

Typing School (Practice Mode):

- 20 progressive lessons from Home Row basics (F/J) to full paragraphs.
- Real-time statistics: Errors counter (❌), Typing Speed (⚡ WPM), and Accuracy (🎯 %).
- Dynamic visual aids (instruction banner, pulsing keycaps, and color-coded active states).
- **Hand Placement Instruction Screen**: Intermediate guide screen showing color-coded home row keys (ASDF and JKL;) along with a CSS slide-in animation of human hand outlines. Includes a "Skip this guide next time" option to toggle local configuration storage.
- Mastery Feedback: Interactive card banner showing congrats/repeat guidelines based on WPM and accuracy thresholds.
- Automatic lesson progression or repetition.

Hybrid Input System:

- Listens to global physical keydown events (Laptops/Desktops).
- Listens to specific pointerdown events on virtual keys (iPads/Tablets).

4. Key Design & Architectural Decisions

During the "Vibe Coding" phase, several crucial iterations were made based on strict visual and usability requirements:

- **The Virtual Keyboard**: Designed to resemble a premium, clean Apple Magic Keyboard. Uses a subtle grid background and soft shadows for a high-end educational feel.
- **The Audio Experience**: Instead of harsh error beeps or generic synth sounds, the app uses a calming "Kalimba/Wind Chime" effect. Correct keystrokes step through a Pentatonic scale (C, D, E, G, A), meaning fast, accurate typing generates beautiful, harmonious melodies.
- **SVG Hand Engine (Historical)**: Initially drawn with a dual-layer SVG path coordinate reach system. Later removed in favor of direct keycap visual styling to eliminate screen clutter.
- **Pulsing Key Highlights & Visual Focus**: Target keys are highlighted dynamically using a pulsing transition (`target-pulse`) styled in touch-typing finger colors.
- **Header Custom Dropdown Centering & Styling**: Replaced the default browser `<select>` dropdown with a custom HTML/CSS list selector. The selector is absolutely centered (`absolute left-1/2 -translate-x-1/2`) within the header. Its button font family (`Nunito`), size (`text-sm`), and colors (slate background, slate border, and 3D shadow) match the header "Menu" button exactly.
- **Option Alignment & Wrapping Prevention**: Dropdown list items are left-aligned with clean padding, styled in Nunito, and configured with `white-space: nowrap` and `text-overflow: ellipsis`. This prevents option labels from wrapping into multi-line text blocks.
- **Clean Spaces (No space symbol `␣`)**: Replaced open-box characters (`␣`) in practice sentences with clean, blank inline-block elements (`.space-char`) of fixed width. The active blue underline renders beneath this empty space. Wrong key presses on spaces trigger a warm amber bottom border.
- **Studio-Grade Typing Colors**:
  - Untyped characters: Muted slate/blue (`#94A3B8`).
  - Active letter: Deep blue cursor underline.
  - Incorrect typing attempt: Text turns amber/gold (`#F59E0B`) to provide real-time feedback.
  - Perfect type (first try): Turns a soft mint green (`#10B981`).
  - Corrected type: Stays amber/gold (`#F59E0B`) to preserve mistake history.
- **Mastery Criteria & Repeat Engine**:
  - L1-L6 (Home Row): Speed >= 10 WPM, Accuracy >= 90%
  - L7-L17 (Top/Bottom Row): Speed >= 15 WPM, Accuracy >= 90%
  - L18-L20 (Advanced): Speed >= 20 WPM, Accuracy >= 90%
  - Failed criteria block progress and guide kids to repeat the lesson with supportive feedback.
- **Interactive Failed Mastery Banner Timer**:
  - Default view duration increased to 8 seconds.
  - Clicking anywhere on the window instantly dismisses the banner and restarts the lesson.
  - Clicking on the banner itself extends the timeout to 14 seconds, giving the user ample time to read the advice.

5. Next Level Development (Roadmap for Full application)

When feeding this file into a full-stack agent (e.g., Google Antigravity), execute the following steps:

I don't want to use heavy technologies for this application just simple things like HTML5 and other js packages for frontend things. Separate resource files if need to save some data instead of backend application or technologies as of now and this is point of discussion at later stage once I am satisfied with the app working.
