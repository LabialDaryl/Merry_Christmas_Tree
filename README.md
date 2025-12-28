
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
