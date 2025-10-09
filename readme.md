# Birthday Greeting Experience

![Animated birthday celebration preview](./images/demo.gif)

## Overview

This repository hosts a fully animated birthday greeting built with plain HTML, CSS, and JavaScript. Opening `index.html` launches an interactive celebration scene: a decorated room with hanging lights, balloons, a cake, and a night sky framed by a window. As visitors follow the on-screen prompts, the page gradually comes to life—lights switch on, music starts, balloons glide across the room, shooting stars streak through the sky, and a heartfelt birthday message appears. The experience concludes by dimming the lights once the message finishes, mirroring the end of a real party.

## Key Features

- **Guided celebration flow** – Visual cues (`clickMe` animations) lead the viewer through each interaction so the experience unfolds in a story-like sequence controlled by `public/javascripts/main.js`.
- **Reactive decorations** – The light bulbs, speakers, cake, floor, and table fade in and out to match the celebration stages using custom `fadeIn` and `fadeOut` helpers.
- **Balloon choreography** – Clicking the balloons triggers coordinated movements: strings release, balloons glide to center stage, then rise individually while looping rotation animations defined in `public/stylesheets/decorations.css`.
- **Shooting-star finale** – `public/javascripts/stars.js` draws a starry sky on a full-screen canvas, repeatedly spawning blinking stars and timed shooting stars (three cycles of 31 meteors) to signal the wish-making moment.
- **Timed birthday message** – After the candle flame is “blown out,” `textLoop` reveals a series of birthday wishes in `index.html`, fading between lines before initiating the closing scene.
- **Ambient soundtrack** – Toggling the speaker plays `audio/hbd.mp3` in a loop, syncing background music with the visual journey.

## Getting Started

1. **Clone or download the project** to your local machine.
2. **Serve the files** through any static web server to ensure audio playback works consistently. For example, from the project root:
   ```bash
   python3 -m http.server 8000
   ```
3. **Open the experience** by visiting `http://localhost:8000/index.html` in your browser.
4. **Follow the prompts** highlighted by the glowing `clickMe` indicators to progress through the celebration.

## Project Structure

- `index.html` – Defines the scene layout, interactive elements, and text content.
- `public/stylesheets/` – Styles for the room, decorations, and animated backgrounds.
- `public/javascripts/main.js` – Controls user interactions, animation timing, and scene transitions.
- `public/javascripts/stars.js` – Renders the starfield and shooting star animations on the canvas backdrop.
- `audio/` – Contains the looping birthday song (`hbd.mp3`).
- `images/` & `imgs/` – Visual assets for the preview GIF and in-page graphics such as balloons, lights, and furniture.

## Customization Tips

- **Update the message:** Edit the `<p>` elements inside the `#message` container in `index.html` to personalize the wishes.
- **Change the soundtrack:** Replace `audio/hbd.mp3` with another audio file and adjust the source path in `public/javascripts/main.js` if needed.
- **Adjust the star show:** Modify the `age` and `cycles` values in `public/javascripts/stars.js` to change how many shooting stars appear.

Enjoy tailoring this interactive greeting to make someone’s birthday extra special!
