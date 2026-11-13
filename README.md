# 🏴‍☠️ Captain Pravin Singh Rajbhar | Interactive 3D Pirate Voyage Portfolio

An interactive, first-person 3D WebGL developer portfolio engineered with **Three.js (`r128`)**, **GSAP 3.12**, **Tailwind CSS**, and the **Native Web Audio API**. Visitors step directly onto the quarterdeck of an exploratory galleon, gripping the helm to navigate an archipelago where each island represents a milestone in **Pravin Singh Rajbhar's** career across Generative AI, Cloud Systems, and Backend Engineering.

---

## 📋 Table of Contents

1. [Project Overview & Design Philosophy](#-project-overview--design-philosophy)
2. [Open-Source Animation Platforms & Sourcing Guide](#-open-source-animation-platforms--sourcing-guide)
3. [Elevated Animation & Transition Architecture](#-elevated-animation--transition-architecture)
4. [Core 3D & Interactive Features](#-core-3d--interactive-features)
5. [Mathematical & Physics Implementation](#-mathematical--physics-implementation)
6. [The Four-Island Career Archipelago](#-the-four-island-career-archipelago)
7. [Recruiter UX & Fast-Track Navigation](#-recruiter-ux--fast-track-navigation)
8. [Controls & Interaction Matrix](#-controls--interaction-matrix)
9. [Built-In 18-Point QA Diagnostic Suite](#-built-in-18-point-qa-diagnostic-suite)
10. [Installation, Customization & Deployment](#-installation-customization--deployment)
11. [Contact & Coordinates](#-contact--coordinates)

---

## 🎯 Project Overview & Design Philosophy

Traditional developer portfolios rely on static 2D scrolling pages that fail to engage technical recruiters in fast-paced screenings. This project transforms a resume into a **spatial, narrative-driven 3D voyage** while strictly adhering to the **5-Second Recruiter Rule**:

* **The "Digital Cartographer / Captain" Archetype:** Merges maritime storytelling (brass compass, mahogany helm, nautical sea-charts, parchment dispatches) with high-clarity technical authority.
* **Split-Complementary Nautical Color Palette:** Deep Oceanic Navy (`#030d14`, `#0284c7`) accented with Antique Brass & Gold Leaf (`#f59e0b`, `#fbbf24`) and semantic milestone highlights (Cyan, Emerald, Ultraviolet, Amber).
* **Zero-Friction Executive Access:** Recruiters can sail interactively, engage hands-free **Auto-Cruise**, or launch the **Recruiter Brief** at any moment for an instant 1-page resume digest.

---

## 🎨 Open-Source Animation Platforms & Sourcing Guide

To achieve high visual appeal without bloated assets, animations across this portfolio combine procedural WebGL physics, CSS keyframe micro-interactions, and GSAP choreographies. Below is a curated directory of premier open-source platforms and asset repositories for discovering and integrating cutting-edge web animations:

| Platform / Source | Asset Type | Best Use Cases | License / Access |
| :--- | :--- | :--- | :--- |
| **[LottieFiles](https://lottiefiles.com/) & [dotLottie](https://dotlottie.io/)** | Lightweight JSON/dotLottie vector animations | Interactive animated icons, compass roses, anchors, weather badges, and parchment unfolding transitions. | Free tier & Open Source community |
| **[Lordicon](https://lordicon.com/)** | Interactive animated vector icons | Micro-interactions on hover/click for ship helms, telescopes, scrolls, swords, and tech badges. | Free tier with attribution |
| **[Shadertoy](https://www.shadertoy.com/) & [GLSL Sandbox](https://glslsandbox.com/)** | Open-source GLSL fragment/vertex shaders | Ocean water reflections, Gerstner waves, caustic light rays, volumetric clouds, and holographic scanlines. | Creative Commons / Open Source |
| **[Three.js Examples](https://threejs.org/examples/) & [Three.js Journey](https://threejs-journey.com/)** | Official Three.js shader, particle, and post-processing templates | Bloom effects, water reflections, instanced meshes, and particle emitters. | MIT License |
| **[Uiverse.io](https://uiverse.io/)** | Community-built CSS/SVG UI components | Cyberpunk holographic borders, glowing glassmorphic cards, radar sonar sweeps, and magnetic buttons. | Open Source (MIT) |
| **[Mixamo by Adobe](https://www.mixamo.com/)** | 3D character models with skeletal animation | Rigged pirate captain, sailing crew, and interactive wheel-steering animations exported to glTF/GLB. | Free for personal & commercial use |
| **[Poly Pizza](https://poly.pizza/) & [Kenney.nl](https://kenney.nl/)** | Low-poly 3D models (CC0 / Public Domain) | Modular naval assets, lighthouses, cannons, tropical vegetation, and treasure chests. | CC0 / Public Domain |
| **[GSAP (GreenSock)](https://gsap.com/) & [anime.js](https://animejs.com/)** | Professional JavaScript animation suites | Spring physics, timeline choreography, elastic easing curves, and camera motion smoothing. | Free / MIT |
| **[Theatre.js](https://www.theatrejs.com/)** | Open-source motion design tool for the web | Visual timeline editor for orchestrating cinematic 3D camera cuts and scene keyframes. | Open Source (Apache 2.0) |

---

## ✨ Elevated Animation & Transition Architecture

### 1. Cinematic Atmospheric GSAP Color Lerping
* **Seamless Sky & Fog Transitions:** Instead of snapping hex values when weather shifts (Day $\rightarrow$ Sunset $\rightarrow$ Night), GSAP smoothly interpolates `scene.background`, `scene.fog.color`, `dirLight.color`, and `renderer.toneMappingExposure` over `2.2 seconds` using `power2.out`.
* **Atmospheric Presets:**
  - **Noon (Day):** Clear Caribbean azure (`#7dd3fc`), crisp sun lighting, exposure `1.1`.
  - **Sunset:** Warm terracotta orange (`#f97316`), deep orange fog (`#c2410c`), golden exposure `1.25`.
  - **Night:** Deep void indigo (`#030712`), volumetric midnight fog (`#020617`), moonlight tint (`#93c5fd`), exposure `0.85`.

### 2. Multi-Layered Particle Systems
* **Ocean Bow Spray Emitter:** Dynamic 200-particle emitter mounted to the clipper bow prow ejecting foaming spray upward and backward as the galleon cuts through the waves, recycling particle lifecycles based on vessel velocity.
* **Stern Wake Foam Trail:** 160 trailing foam particles issuing from the stern rudder, gently drifting outward and dispersing across the sea surface.
* **Carronade Muzzle Smoke:** 80 expanding volumetric smoke particles bursting sideways from active carronades upon firing, with randomized velocity and gradual alpha fade.
* **Twinkling Starfield:** 1,200 particle stars populating the night skybox dome, smoothly fading to full luminance during the Night atmospheric cycle.
* **Bioluminescent Ocean Plankton:** 300 additive cyan particles drifting near the water surface, creating a glowing ethereal wake at night.

### 3. Tactile Nautical HUD Micro-Interactions
* **Live Interactive Brass Compass:** An antique compass dial mounted in the top-left HUD dynamically rotates in real time based on `(shipGroup.rotation.y + cameraYaw)`, always pointing true magnetic North with digital degree/cardinal readout.
* **Tactical Sonar Radar Minimap:** Positioned in the bottom-left, featuring concentric range rings, a 360° phosphor beam sweep, and active clickable ping blips tracking all 4 milestone islands relative to the ship.
* **Equalizer Soundwave Visualizer:** When ambient waves are toggled ON, a 5-bar responsive equalizer visualizer animates in rhythm with the wave frequency.
* **Dynamic Knots Speedometer:** Responsive velocity readout (`13.5 - 18.2 KTS`) reflecting cruise and acceleration momentum.

### 4. Fluid GSAP Spring Modal Choreography
* **Spring Elastic Entrances:** Modals emerge with a backdrop blur fade and an elastic scale animation (`scale: 0.92 -> 1.0`, `back.out(1.5)`).
* **Graceful Exit:** Instant, smooth fade and scale-down (`scale: 0.94`, `power2.in`) with keyboard `Escape`, backdrop tap, or close buttons.

---

## 🌟 Core 3D & Interactive Features

### 1. First-Person Maritime Helm & Galleon Quarterdeck
* **Ship Architecture:** Tiered mahogany hull, tumblehome bulwarks, gold-leaf waterline strakes, clipper bow prow, bowsprit spar, raised poop deck with turned brass balusters, captain's sea-chart table, naval carronades, coiled ropes, cargo barrels, and sternpost lanterns.
* **Dynamic Rigging & Wheel:** Master 8-spoke wooden wheel tilts dynamically with helm steering and swell roll, while the main mast pennant flag flutters in procedural wind.

### 2. Captain's Spyglass / Telescope Mode
* **Precision Long-Range Scouting:** Press `[T]` or click the Spyglass HUD button to smoothly lerp camera FOV from 60° down to 24° (2.5x optical magnification) using GSAP easing.
* **Authentic Brass Reticle Viewfinder:** Displays dual-ring antique brass crosshairs, depth measurement ticks, nautical compass bearing, and a circular vignette mask with a slight camera glance towards nearby archipelago landmarks.

### 3. Interactive Naval Carronades (Deck Cannons)
* **Direct Raycasting & Hotkey Firing:** Aim and click directly on the port or starboard deck cannons, press `[F]`, or click the HUD **"Fire Cannon"** button.
* **Recoil, Smoke & Audio VFX:** Triggers realistic carriage recoil along the deck via GSAP, bursts volumetric muzzle smoke outward, and synthesizes a procedural Web Audio acoustic cannon blast.

### 4. Flocking Seagulls Wildlife System
* **Procedural Low-Poly Avian Flock:** 6 procedural low-poly seagulls soaring and circling above the milestone archipelago islands, featuring animated wing-flapping kinematics synchronized with scene delta time.

### 5. In-World 3D Holographic Monoliths & Raycasting
* **Procedural Canvas Textures:** $1024 \times 1024$ `THREE.CanvasTexture` maps rendered with cyber-scanlines, tech brackets, glowing gradient borders, and wrapped bullet points onto double-sided obsidian monoliths.
* **Bilateral Raycasting:** Click directly on any 3D monolith in the viewport—or its screen-projected HUD pin—to sail smoothly to that landmark and inspect its dossier.
* **Proximity Glance Engine:** Sailing within $260\text{ units}$ of a landmark triggers a HUD alert and smoothly glances the helm camera toward the monument.

### 6. Procedural Web Audio Soundscapes (Zero External Audio Files)
* **Ocean Wave Surf Synthesizer:** Realistic ambient surf synthesized via Web Audio Pink Noise buffer routed through a biquad lowpass filter ($380\text{ Hz}$) modulated by a $0.22\text{ Hz}$ LFO.
* **Naval Cannon Blast Synthesizer:** Multi-layered explosive rumble using low-frequency decaying noise bursts with rapid frequency modulation.
* **Harmonic Ship's Bell:** Additive 3-tone acoustic bell chime ($587\text{ Hz}, 1174\text{ Hz}, 1762\text{ Hz}$) triggering upon archipelago waypoint arrivals or manual chime.

---

## 📐 Mathematical & Physics Implementation

### 1. Collision-Free Navigational Fairway (`CatmullRomCurve3`)
The voyage follows a 5-anchor `THREE.CatmullRomCurve3` strictly confined to the central sea corridor ($X \in [-10, +10]$), providing $>145\text{ units}$ clearance from all archipelago islands:
* **Origin ($t = 0.00$):** $(0, 0, 0)$ — Open Caribbean Waters
* **Waypoint 1 ($t = 0.18$):** $(10, 0, -180)$ — Starboard clearance $145\text{ units}$ to Island 1
* **Waypoint 2 ($t = 0.45$):** $(-10, 0, -420)$ — Port clearance $145\text{ units}$ to Island 2
* **Waypoint 3 ($t = 0.72$):** $(8, 0, -680)$ — Starboard clearance $147\text{ units}$ to Island 3
* **Anchorage ($t = 1.00$):** $(0, 0, -920)$ — Safe halt $130\text{ units}$ shy of Island 4 $(0, 0, -1050)$

### 2. Multi-Frequency Ocean Wave Displacement
Subdivided $1600 \times 1600$ plane with $128 \times 128$ segments ($16,641$ vertices). Vertex elevation $y(u, w, t)$ is evaluated each frame via trigonometric interference:

$$y(u, w, t) = y_0 + 0.7 \sin(0.035u + 1.8t) + 0.8 \cos(0.025w + 1.3t) + 0.5 \sin(0.015(u + w) + 0.9t)$$

### 3. Vessel Buoyancy & Damped Interpolation
* **Spline Momentum:** Voyage progress `currentT` interpolates toward `targetT` with exponential damping ($\Delta t \times 0.06$).
* **Heave, Pitch & Roll:** Oceanic swell is simulated via vertical heave ($0.25 \sin(2.0t)$), pitch ($0.025 \cos(1.6t)$), and roll ($0.035 \sin(1.4t)$).

---

## 🏝️ The Four-Island Career Archipelago

| Island | Spline Anchor | Coordinates $(X, Y, Z)$ | 3D Monuments & Landmarks | Career Milestone & Core Stack |
| :--- | :--- | :--- | :--- | :--- |
| **01. Cloud Genesis** | `t = 0.18` | `(155, 0, -180)` | Stepped Mayan stone terraces, 5 server racks with glowing cyan LED blades, orbiting data ring | **BCA in Cloud Tech & InfoSec** — ITM University, Raipur (**87.30% Distinction**). AWS, Docker, Python, Java, C/C++, MySQL. |
| **02. InfoSec Bastion** | `t = 0.45` | `(-155, 0, -420)` | Stone citadel walls, twin watchtowers with crimson roofs, iron portcullis, rotating wireframe geodesic firewall dome | **Backend Development Intern** — Wholiex Enterprise (Boston, US Remote). Django REST APIs, PostgreSQL, PostHog, Azure Blob Storage, Firebase, Swagger. |
| **03. Gen AI Sanctuary** | `t = 0.72` | `(155, 0, -680)` | Stepped obsidian pyramid temple, gold-trimmed columns, levitating amethyst octahedron neural core & counter-rotating ring | **MCA in Generative AI** — Alliance University, Bengaluru. F1 Reinforcement Learning Simulation, Marketing AI Platform, Hack to Crack 2.0. |
| **04. The Anchorage** | `t = 0.96` | `(0, 0, -1050)` | Red-and-white stone lighthouse with rotating volumetric beacon cone, timber pier pilings, cargo crates | **Harbor Destination & Hiring Dispatch** — Direct email, phone, GitHub, and LinkedIn contact coordinates. |

---

## 💼 Recruiter UX & Fast-Track Navigation

* **Captain's Welcome Dispatch:** Launches on initial visit with a 4-point itinerary and quick **"Take The Helm"** or **"Executive Brief"** launch options.
* **Executive Brief Modal:** Clean, scannable resume dossier highlighting academic honors, production internship bullet points, AI project summaries, and one-click contact actions.
* **Hands-Free Auto-Cruise:** Toggle **"Cruise"** in the top HUD for effortless forward navigation (`targetT += delta * 0.025`).
* **Screen-Projected Floating HUD Pins:** Dynamic 2D glassmorphic badges track each island in screen space (`Vector3.project(camera)`), scaling and fading smoothly by distance.

---

## 🎮 Controls & Interaction Matrix

| Input Method | Action |
| :--- | :--- |
| **Mouse Wheel (Scroll Down / Up)** | Sail forward ($0\% \rightarrow 100\%$) or backtrack along fairway |
| **Click & Drag / Touch Swipe** | Rotate helm camera yaw/pitch and steer the ship's wheel |
| **Click on 3D Monolith / HUD Tag** | Sail directly to that island and open its detailed logbook modal |
| **Click on Deck Cannons** | Raycast & fire the port/starboard carronades with recoil & smoke VFX |
| **`T` Key / Spyglass Button** | Toggle Captain's Spyglass 2.5x optical zoom viewfinder (`camera.fov: 60° -> 24°`) |
| **`F` Key / "Fire Cannon" Button** | Fire port/starboard naval carronades with acoustic blast & muzzle smoke |
| **`W` / `S` or `↑` / `↓` Keys** | Step forward or backward along voyage spline |
| **`A` / `D` or `←` / `→` Keys** | Pan camera view left (port) or right (starboard) |
| **Click Radar Blip / Compass** | Fast-travel to archipelago island or snap heading true North |
| **Bottom Voyage Scrubber** | Scrub immediately to any percentage ($0\% - 100\%$) of the journey |
| **`Esc` Key** | Dismiss any active modal, spyglass viewfinder, or diagnostic drawer |

---

## 🧪 Built-In 18-Point QA Diagnostic Suite

Clicking **"Run QA Suite"** executes an automated 18-point integration test suite (`runPortfolioTestSuite()`) directly inside the browser:

1. **WebGL 2.0 / 1.0 Context Active** — Verifies valid rendering context initialization.
2. **Three.js Scene Graph Mounted** — Confirms scene children are populated.
3. **GSAP Animation Engine Loaded (3.12+)** — Verifies GSAP timeline and easing engine is available.
4. **Camera Rigged at Eye-Level** — Ensures first-person camera height stays safely above deck.
5. **Catmull-Rom Spline Anchor Points** — Validates all 5 fairway control vectors.
6. **Ship Group Buoyant on Deck** — Asserts vessel draft remains above water level.
7. **Rotatable Ship's Wheel Assembled** — Checks wheel rim, hub, and 8 spoke assemblies.
8. **Ocean Bow Spray Particles Mounted** — Asserts active bow foam particle emitter.
9. **Stern Wake Foam Particles Active** — Confirms trailing wake foam particle system.
10. **Twinkling Starfield Active** — Confirms $>1,000$ skybox star particles.
11. **Dynamic Caribbean Ocean Mesh Subdivided** — Confirms $>10,000$ wave vertices.
12. **Flocking Seagulls Life System** — Confirms 6 procedural low-poly birds with animated flapping wings.
13. **Interactive Naval Carronades Mounted** — Validates port and starboard deck cannon groups.
14. **Island 1: Cloud Genesis Initialized** — Validates server monoliths and landmass.
15. **Island 2: InfoSec Bastion & Shield** — Confirms wireframe geodesic shield reference.
16. **Island 3: Gen AI Neural Core** — Verifies levitating amethyst core mesh.
17. **Island 4: Harbor Lighthouse Beacon** — Checks rotating beacon light cone.
18. **Credential Integrity (BCA 87.30% & MCA Gen AI)** — Asserts accurate resume badges.

---

## 🚀 Installation, Customization & Deployment

### Local Execution
Zero build tools or package managers required:
```bash
# Clone or navigate to the directory
cd Portfolio

# Launch with any local server
npx serve .
# or
python -m http.server 8080
```

### Static Hosting
Deploy `index.html` directly to **GitHub Pages**, **Vercel**, **Netlify**, or **Cloudflare Pages** with zero configuration.

---

## 📬 Contact & Coordinates

* **Captain / Developer:** Pravin Singh Rajbhar
* **Location:** Bengaluru, Karnataka, India
* **Email:** `spravinMCA25@stu.alliance.edu.in`
* **Phone:** `+91 8989082556`
* **GitHub:** [github.com/pravinSinghh](https://github.com/pravinSinghh)
* **LinkedIn:** [linkedin.com/in/pravin-singh-rajbhar](https://linkedin.com/in/pravin-singh-rajbhar)
