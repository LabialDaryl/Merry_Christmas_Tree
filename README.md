# 🎄 Grand Luxury Interactive Christmas Tree

An immersive, high-fidelity 3D Christmas tree experience featuring hand gesture control, dynamic chaos-to-order assembly, and luxurious emerald and gold aesthetics.

## 📝 Prompt

Gemini 3 in Google AI Studio and Claude 4.5 Sonnet in Cursor:

```
Character setup: You are a skilled React 19, TypeScript, and Three.js (R3F) creative developer expert. The task goal: Build a Web application named "Grand Luxury Interactive Christmas Tree" with high fidelity 3D visuals, luxurious emerald and gold aesthetics, and a Trump-style feel.

Tech stack: React 19, TypeScript, React Three Fiber, Drei, Postprocessing, Tailwind CSS.

Core logic and architecture: State machine: Include CHAOS (Chaos scatter) and FORMED (Assembly into a tree) two states, and transition between them dynamically. Dual-Position System: All elements (leaf, decorations) are initialized and assigned two coordinates: ChaosPosition: Random coordinates in a spherical space. TargetPosition: Target coordinates that form the conical shape of the tree.
In useFrame, interpolate between the two using Lerp. Specific implementation details: Foliage system (Foliage): Render a large number of particles using THREE.Points and custom ShaderMaterial. Decoration system (Ornaments): Optimize rendering using InstancedMesh. Group into various colored gift boxes (heavy), various colored baubles (light), and various decorative lights (very light), each with different physical push weights. Use Lerp for smooth repositioning animations. Post-processing: Enable Bloom effect (threshold 0.8, intensity 1.2) to create a warm "golden halo".
Scene configuration: Camera position [0, 4, 20]. Use Lobby HDRI environment lighting.
Inside, add many Polaroid-style decorations.
Use the camera to detect hand gestures, and unleash represents unleash when the hand is open, and restore to the tree when closed. Adjust the view using hand movement.
```

## 🛠️ Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd grand-luxury-interactive-christmas-tree
   ```

2. **Install dependencies:**
   ```bash
   # 🎄 Grand Luxury Interactive Christmas Tree

   An immersive, high-fidelity 3D Christmas tree experience featuring hand gesture control, dynamic chaos-to-order assembly, and luxurious emerald and gold aesthetics.

   ## 📝 Prompt

   Gemini 3 in Google AI Studio and Claude 4.5 Sonnet in Cursor:

   ```
   Role: You are a 3D creative development expert proficient in React 19, TypeScript, and Three.js (R3F).
   Task goal: Build a high-fidelity 3D web application called "Grand Luxury Interactive Christmas Tree". The visual style should convey a luxurious, "Trump-esque" feel with primary colors of deep emerald green and highlight gold, accompanied by cinematic bloom/glow effects.
   Tech stack: React 19, TypeScript, React Three Fiber, Drei, Postprocessing, Tailwind CSS.

   Core logic & architecture:
   - State machine: includes CHAOS (scattered) and FORMED (assembled) states and dynamically morphs between them.
   - Dual-Position System: All elements (needles, ornaments) are assigned two coordinates at initialization:
     - ChaosPosition: random coordinates within a spherical volume.
     - TargetPosition: target coordinates that form the tree cone shape.
   During `useFrame`, interpolate (lerp) between these positions according to progress.

   Implementation details:
   - Foliage: render many particles using `THREE.Points` and a custom `ShaderMaterial`.
   - Ornaments: use `InstancedMesh` for rendering performance. Group into heavier gift boxes (various colors), lighter baubles (various colors), and tiny accent lights (very light), each with different physics push weights. Use lerp for smooth repositioning animations.
   - Postprocessing: enable Bloom (threshold 0.8, intensity 1.2) to create a warm "golden halo".

   Scene configuration: camera position `[0, 4, 20]`, using a Lobby HDRI for environment lighting.
   Include many polaroid-style photos as decorations.
   Use the camera for hand gesture detection: opening the hand represents "unleash" (CHAOS), closing returns to the formed tree. Hand movements can adjust the camera/view.
   ```

   ## 🛠️ Installation

   1. **Clone the repository:**
      ```powershell
      git clone <repository-url>
      cd grand-luxury-interactive-christmas-tree
      ```

   2. **Install dependencies:**
      ```powershell
      npm install
      ```

   3. **Run the development server:**
      ```powershell
      npm run dev
      ```
   
      > 📝 Note: Local dev mode uses `localStorage` for sharing (works in the same browser only).
      > For full cloud sharing, see step 4.

   4. **Configure Cloudflare (Optional - for cloud sharing):**
      - Follow the detailed guide in `cloudflare-setup.md` (if present).
      - Copy `env.example` to `.env.local` and fill in your Cloudflare credentials.
      - Use `npm run dev:vercel` to test with a full Vercel environment.

   5. **Open your browser:**
      - Navigate to `http://localhost:3010`.
      - Allow camera access for gesture control.
      - Click the **`Upload Photos`** button to upload your photos.


   ## 🎯 Usage

   ### Photo Upload & Sharing

   1. **Upload Photos:**
      - Click the **`Upload Photos`** button to select up to 22 images.
      - Photos will appear as polaroids on the Christmas tree.

   2. **Generate Share Link:**
      - After uploading photos, click **`Generate Share Link`**.
      - Wait 2–3 seconds for the upload to complete.
      - Copy the generated link and share it with friends.

   3. **View Shared Photos:**
      - Friends can open the share link in any browser.
      - Photos will automatically load on the Christmas tree.
      - No login or app installation required.
      - Links expire after 30 days.

   ### Gesture Controls

   1. **Position your hand** in front of the webcam (visible in the top-right preview).
   2. **Move your hand** to control the camera angle:
      - Left/Right: Horizontal rotation
      - Up/Down: Vertical tilt
   3. **Open your hand** (spread all fingers): Enter unleash (CHAOS) mode.
   4. **Close your fist**: Restore the tree to formed mode.

   ### Mouse Controls

   When no hand is detected, you can:
   - **Click and drag** to rotate the view
   - **Scroll** to zoom in/out
   - **Right-click and drag** to pan (disabled by default)

   ## 🏗️ Tech Stack

   ### Frontend
   - React 19 with TypeScript
   - React Three Fiber (R3F) for 3D rendering
   - Three.js for WebGL graphics
   - `@react-three/drei` for helpers
   - `@react-three/postprocessing` for visual effects
   - MediaPipe for hand gesture detection
   - Tailwind CSS for styling

   ### Backend (Photo Sharing)
   - Vercel Serverless Functions
   - Cloudflare R2 (S3-compatible object storage)
   - Cloudflare KV (key-value storage)
   - AWS SDK S3 Client for R2 integration

   ### Features
   - Hand gesture control via webcam
   - Dynamic state transitions (CHAOS ↔ FORMED)
   - Photo upload and cloud sharing
   - Temporary share links (30-day expiration)
   - Instanced rendering for performance
   - Bloom and post-processing effects

   ## 🎅 Happy Holidays!

   May your code be merry and bright! 🎄✨

   ````
   - Follow the detailed guide in `cloudflare-setup.md`.
   - Copy `env.example` to `.env.local` and fill in your Cloudflare credentials.
   - Use `npm run dev:vercel` to test with a full Vercel environment.

5. **Open your browser:**
   - Navigate to `http://localhost:3010`.
   - Allow camera access for gesture control.
   - Click the **`Upload Photos`** button to upload your photos.


## 🎯 Usage

### Photo Upload & Sharing

1. **Upload Photos:**
   - Click the **`Upload Photos`** button to select up to 22 images.
   - Photos will appear as polaroids on the Christmas tree.

2. **Generate Share Link:**
   - After uploading photos, click **`Generate Share Link`**.
   - Wait 2–3 seconds for the upload to complete.
   - Copy the generated link and share it with friends.

3. **View Shared Photos:**
   - Friends can open the share link in any browser.
   - Photos will automatically load on the Christmas tree.
   - No login or app installation required.
   - Links expire after 30 days.

### Gesture Controls

1. **Position your hand** in front of the webcam (visible in the top-right preview).
2. **Move your hand** to control the camera angle:
   - Left/Right: Horizontal rotation
   - Up/Down: Vertical tilt
3. **Open your hand** (spread all fingers): Enter unleash (CHAOS) mode.
4. **Close your fist**: Restore the tree to formed mode.

### Mouse Controls

When no hand is detected, you can:
- **Click and drag** to rotate the view
- **Scroll** to zoom in/out
- **Right-click and drag** to pan (disabled by default)

## 🏗️ Tech Stack

### Frontend
- React 19 with TypeScript
- React Three Fiber (R3F) for 3D rendering
- Three.js for WebGL graphics
- `@react-three/drei` for helpers
- `@react-three/postprocessing` for visual effects
- MediaPipe for hand gesture detection
- Tailwind CSS for styling

### Backend (Photo Sharing)
- Vercel Serverless Functions
- Cloudflare R2 (S3-compatible object storage)
- Cloudflare KV (key-value storage)
- AWS SDK S3 Client for R2 integration

### Features
- Hand gesture control via webcam
- Dynamic state transitions (CHAOS ↔ FORMED)
- Photo upload and cloud sharing
- Temporary share links (30-day expiration)
- Instanced rendering for performance
- Bloom and post-processing effects

## 🎅 Happy Holidays!

May your code be merry and bright! 🎄✨

````
