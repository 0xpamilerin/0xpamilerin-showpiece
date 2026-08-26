# 0xpamilerin - Frontend Developer Portfolio

This project is a single-page, interactive portfolio landing page for a Frontend Developer (0xpamilerin). It is designed to be highly visual, featuring modern web aesthetics, smooth CSS animations, and an interactive particle background.

## Tech Stack

The project is built entirely with core web technologies, ensuring high performance without the need for external frameworks or libraries (other than web fonts):

- **HTML5**: Semantic structure.
- **CSS3**: Advanced styling, custom properties (variables), Flexbox, gradients, filters (glow, blur), and complex `@keyframes` animations.
- **JavaScript (Vanilla)**: Object-oriented particle system, typing effects, and basic DOM interactions.

## Architecture & Features

### 1. Typography and Theming
- Uses **Google Fonts**: `Inter` for general UI text and `JetBrains Mono` for code-like decorative elements and skill pills.
- A central `--root` block in the CSS defines the color palette using CSS variables (e.g., `--bg`, `--accent`, `--accent-2`), making the theme easy to modify.

### 2. Interactive Particle Background
- A `<canvas>` element sits fixed at the lowest z-index (`z-index: 0`).
- **JavaScript Particle System**: A `Particle` class generates nodes that float around the screen. 
- **Connections**: When particles get close to one another, a line is drawn between them, creating a network effect.
- **Mouse Interaction**: The particles detect the mouse position and are gently repelled away, creating an interactive, physical feel.

### 3. Visual Layers and Overlays
- **Scanlines**: A `repeating-linear-gradient` overlays the entire screen (`z-index: 2`) with `pointer-events: none` to give the page a subtle, retro CRT monitor aesthetic.
- **Geometric Orbit**: Three nested rings with dots rotate at different speeds and directions in the background using CSS `animation` and `transform: rotate`.

### 4. Animated Content Flow
The content reveals itself sequentially using carefully timed CSS animations (`fade-in`, `slide-up`, `pill-in`, `name-in`):
- **Greeting**: Uses a JavaScript typing effect (`> Hello, World...`) combined with a blinking CSS cursor.
- **Nameplate**: Features a large gradient text (`background-clip: text`) with an animated gradient shift and a hover "glitch" effect.
- **Skill Pills**: A staggered entrance animation displays the developer's core competencies.
- **Decorative Code Blocks**: Fixed in the corners, adding to the developer persona.

### 5. Call to Action & Status Bar
- The **CTA Button** uses nested gradients and pseudo-elements (`::before`) with `filter: blur` to create a glowing effect on hover.
- A **Status Bar** sits at the bottom showing availability, location (Ibadan, Nigeria), and versioning. It features a pulsing green dot to indicate an "online" or "available" status.

## How to Run

Because the project relies purely on static front-end files without a build step or external dependencies:

1. Clone or download the repository.
2. Open the `index.html` file directly in any modern web browser.
3. (Optional) Run it via a local development server (like VS Code Live Server, or Python's `http.server`) if you wish to expand it with external module imports in the future.
