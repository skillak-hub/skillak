Skillak Hub — Google Meet Edition

1) Install dependencies:
   npm install

2) Create a .env file from .env.example and fill the Google OAuth values.

3) Enable Google Meet API in Google Cloud for the same project.

4) Run the server:
   npm start

5) Open:
   http://localhost:3000

Meeting flow:
- Clicking session entry creates a fresh Google Meet space for that booking.
- The link is stored in Firestore and shown to both sides.
- The platform runs a 60-minute countdown.
- At the end, the app calls the Meet end endpoint and closes the booking.

Files added/updated:
- server.js (Meet create/end API)
- assets/scripts/meet-session.js (booking → Meet bridge)
- sw.js (cache updated files)
- .env.example (Google env template)

Important:
- Never put Google client secret in frontend code.
- Rotate any secret that was exposed publicly.
