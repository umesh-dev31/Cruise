# Cruise

An interactive, scroll-driven 3D web experience built for NAVIS Luxury Cruises and Ship Manufacture. Combining multi-stage image sequence canvas scrubbing, real-time WebGL ocean wave simulation, GSAP scroll triggers, and sleek modern UI architecture.

---

## Live Repository

[https://github.com/umesh-dev31/Cruise](https://github.com/umesh-dev31/Cruise)

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Next.js 16 (App Router) | React framework and production build tooling |
| React 19 | UI component architecture and state management |
| Three.js | WebGL 3D rendering engine |
| @react-three/fiber | Declarative Three.js scene graph for React |
| @react-three/drei | Three.js shader and helper primitives |
| GSAP + ScrollTrigger | Scroll-driven timeline orchestration and frame scrubbing |
| Lenis | Smooth momentum-based inertia scrolling |
| Tailwind CSS v4 | Modern utility-first styling and theme tokens |
| TypeScript | Type safety and component interfaces |

---

## Project Structure

```
cafe-3d-scroll/
  src/
    app/
      globals.css               Global CSS variables, grain overlays, typography
      layout.tsx                Root layout with metadata and font configurations
      page.tsx                  Main composite page assembling all sections
    components/
      Preloader.tsx             Interactive asset preloader with real-time progress
      ScrollCanvas.tsx          Hero canvas: 300-frame scroll-driven sequence
      OceanScene.tsx            Interactive Three.js 3D ocean wave simulation
      OceanSceneWrapper.tsx     Client dynamic loader wrapper for OceanScene
      ThirdScrollCanvas.tsx     Secondary 300-frame voyage scroll story sequence
      FifthScrollCanvas.tsx     Shipbuilding and engineering scroll sequence
      CookingScrollCanvas.tsx   Culinary and dining scroll experience sequence
      FeatureCards.tsx          Luxury cabins, dining, and pool deck showcase cards
      NightlifeBento.tsx        Nightlife, club, and lounge bento grid
      PoolGallery.tsx           Interactive pool deck image and amenity gallery
      ExpandingGallery.tsx      Smooth expanding image preview grid
      AboutStats.tsx            Shipyard statistics and maritime credentials
      SpaceMarquee.tsx          Smooth scrolling architectural marquee
      SiteAnimations.tsx        Global GSAP entry and reveal animations
  public/
    hero section scroll/        300 high-resolution JPEG frames for hero sequence
    third section scroll/       300 frames for voyage showcase sequence
    fifith scroll section/      300 frames for design and engineering sequence
    ship models/                Luxury cabin, pool, and deck photography
    food/                       Fine dining and culinary assets
    the space/                  Interior architectural photography
    designed for better experinece/ Hero and marketing backdrop imagery
```

---

## Key Features and Architecture

### 1. High-Performance Scroll-Driven Canvases
- **Preloaded Frame Sequences:** Each sequence utilizes 300 sequential frames scrubbed against window scroll depth.
- **GSAP ScrollTrigger:** Pins the viewport while scrubbing through normalized frame indices, aligning synchronized textual narrative overlays at exact milestones.
- **Device Pixel Ratio Scaling:** Canvases automatically detect display DPI and render crisp visuals while preventing memory thrashing.

### 2. Real-Time 3D Ocean Simulation
- **Dynamic Wave Displacement:** Custom plane geometry evaluated every frame using compound trigonometric wave functions in @react-three/fiber.
- **Wireframe Grid and Particle Canopy:** Layered wireframe terrain and ambient floating particles to convey maritime engineering depth.
- **Client Dynamic Loading:** Canvas elements are dynamically loaded on the client side with SSR disabled to guarantee smooth WebGL initialization.

### 3. Modular Luxury Experience Showcase
- **Bento Grids:** Clean modular arrangements highlighting nightlife, deck lounges, and state-of-the-art amenities.
- **Responsive Layout:** Optimized for cross-device consistency with touch-friendly interactions and fluid typography.
- **Inertia Scrolling:** Unified scroll physics powered by Lenis for frictionless acceleration and deceleration.

---

## Getting Started

### Prerequisites

- Node.js 18.0.0 or higher
- npm, pnpm, or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/umesh-dev31/Cruise.git
cd Cruise
```

2. Install dependencies:
```bash
npm install
```

3. Launch the development server:
```bash
npm run dev
```

4. Open your browser and navigate to:
```
http://localhost:3000
```

---

## Build and Deployment

To generate a standalone production build:

```bash
# Create optimized production build
npm run build

# Start the production server
npm run start
```

---

## Scripts

| Command | Action |
|---|---|
| npm run dev | Starts Next.js development server on port 3000 |
| npm run build | Creates an optimized production build |
| npm run start | Runs the production build server |
| npm run lint | Runs ESLint check across all files |

---

## License

This project is open source and available under the MIT License.
