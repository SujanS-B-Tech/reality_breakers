# REALITY BREAKERS — Multiplayer Expo Game

A cooperative browser game for a laptop and students' phones. One player creates a room; teammates join from phones using a six-character room code. Every player has a different ability.

## Deploy to Vercel (static website)
This project is static HTML and can be deployed on Vercel without a server backend.

### Option 1: Deploy with Vercel CLI
1. Install Node.js from https://nodejs.org/
2. Open a terminal in this folder.
3. Run:
   ```bash
   npm install -g vercel
   vercel
   ```
4. Follow the prompts and choose the default settings. When asked about the project directory, use the current folder. Framework preset: Other. Build command: leave blank. Output directory: `public`.
5. After the preview deployment succeeds, run:
   ```bash
   vercel --prod
   ```
6. Vercel prints the public website URL. Share that URL with students.

### Option 2: Deploy using the Vercel website
1. Put this folder in a GitHub repository.
2. Sign in at https://vercel.com/ and choose **Add New → Project**.
3. Import the repository.
4. Set Framework Preset to **Other** and Output Directory to `public`; no build command is required.
5. Click **Deploy**.

## How to play
1. Open the deployed URL on the laptop.
2. Click Create Game. Share the six-character room code.
3. Teammates open the same URL on their phones and enter the room code and a name.
4. Start the mission with at least two players.
5. Roles: Time Controller freezes glitches; Reality Shifter toggles the bridge; Energy Master charges nodes; Portal Creator opens the portal; Explorer moves the character.
6. Charge all three nodes, open the portal, and move the Explorer to the exit before the timer ends.

## Multiplayer note
This static build uses PeerJS's public cloud signaling service and WebRTC peer-to-peer data connections, so devices need internet access. Network/firewall restrictions may prevent peer connections on some expo Wi-Fi networks. Test the deployed link on the actual laptop and phones before the event.

## Known implementation details
- No account, app install, camera, or special hardware required.
- Up to five players per room.
- Browser-only game state, shared by the host laptop.
- This is an expo prototype. Test multiplayer on your target devices before relying on it in a live event.
