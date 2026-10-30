# Zentry Gaming Website Clone

## Description

A polished, single-page marketing experience that recreates the look and feel of the Zentry gaming universe. It is built to demonstrate how a developer can turn a bold visual design into a living, scrollable, and interactive website.

## Overview

Zentry helps developers showcase high-impact gaming and entertainment brands through one continuous, animated landing experience. It combines full-screen video, scroll-driven scene changes, and reactive mouse effects into a page that feels like a native product reveal. Teams can use it as a starting point for any campaign that needs to keep visitors scrolling and exploring.

## System Architecture

```mermaid
flowchart LR
    User["Visitor"]
    WebApp["Interactive React App"]
    ScrollEngine["Smooth Scroll Engine"]
    AnimationEngine["GSAP Animation Engine"]
    MediaAssets["Media Assets"]

    User --> WebApp
    WebApp --> ScrollEngine
    WebApp --> AnimationEngine
    ScrollEngine --> WebApp
    AnimationEngine --> MediaAssets

    style User fill:#0f172a,stroke:#64748b,stroke-width:2px,color:#fff
    style WebApp fill:#1e1b4b,stroke:#6366f1,stroke-width:2px,color:#fff
    style ScrollEngine fill:#2e1065,stroke:#8b5cf6,stroke-width:2px,color:#fff
    style AnimationEngine fill:#2e1065,stroke:#8b5cf6,stroke-width:2px,color:#fff
    style MediaAssets fill:#451a03,stroke:#f59e0b,stroke-width:2px,color:#fff
```

## Features

- **Cinematic hero section** with switchable full-screen video loops and a custom loading spinner.
- **Scroll-driven pinned storytelling** that locks the viewport while text points reveal in sequence.
- **Mouse-reactive 3D tilt** on the story image based on cursor position.
- **Smooth inertial scrolling** across the entire page for a premium navigation feel.
- **Animated headings** that flip into view as they enter the viewport.
- **Audio toggle** for background ambience directly from the navbar.
- **Bento-style features grid** with hover-tilt cards and looping video backgrounds.
- **Responsive layout** that adapts cleanly from mobile to desktop.

### Cinematic Hero Video Switching

Clicking the small preview clip swaps the main hero background with a smooth fullscreen expansion.

```mermaid
sequenceDiagram
    actor User
    participant App
    participant VideoLayer

    User->>App: Clicks mini preview clip
    App->>VideoLayer: Loads next hero video
    VideoLayer-->>App: Video ready
    App->>VideoLayer: Expands clip to fullscreen
    VideoLayer->>User: New hero background plays
```

### 3D Story Image Tilt

Moving the cursor over the story image creates a live 3D perspective shift.

```mermaid
sequenceDiagram
    actor User
    participant App
    participant Image

    User->>App: Moves mouse over story image
    App->>App: Calculates cursor offset from center
    App->>Image: Applies 3D rotateX and rotateY
    Image->>User: Image tilts toward cursor
    User->>App: Mouse leaves image
    App->>Image: Resets tilt to flat
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/numcodes/zentry-clone.git
cd zentry-clone
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

The site will be available at `http://localhost:5173` by default.

## Usage

Open `http://localhost:5173` in your browser and scroll through the page.

- Click the small preview video in the hero to swap the main background clip.
- Hover over the story image to see the live 3D tilt effect.
- Use the audio indicator in the navbar to toggle background ambience.
- Navigate between sections using the navbar links.

![Zentry preview](/public/preview.png)

## Technologies Used

| Technology | Description |
| :--- | :--- |
| [React](https://react.dev/) | Component-based UI library |
| [TypeScript](https://www.typescriptlang.org/) | Typed JavaScript for safer code |
| [Vite](https://vitejs.dev/) | Fast build tool and dev server |
| [Tailwind CSS](https://tailwindcss.com/) | Utility-first styling |
| [GSAP](https://gsap.com/) | Advanced animations and scroll triggers |
| [Locomotive Scroll](https://locomotivemtl.github.io/locomotive-scroll/) | Smooth, inertial scrolling |
| [React Icons](https://react-icons.github.io/react-icons/) | SVG icon library |

## Contributing

Contributions are welcome. Feel free to fork the repository, create a feature branch, and open a pull request with your changes.

## Author

- LinkedIn: [Ugochukwu Nweze](https://linkedin.com/in/ugochukwu-nweze-08812a2b8)
- X: [@CodesNum80638](https://x.com/CodesNum80638)

## Badges

[![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=white)](https://gsap.com/)
