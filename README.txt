Soft Dial PWA starter

Files:
- index.html: UI, CSS and JavaScript in one file
- manifest.json: PWA manifest
- sw.js: offline app-shell service worker

Important:
1. Host these files on HTTPS (GitHub Pages or Vercel).
2. Browser calling requires your SIP provider to support SIP over secure WebSocket (WSS) and WebRTC.
3. The SIP domain alone is not a WSS endpoint. Ask Sarker Communication for:
   - WSS/WebSocket URL (for example wss://host:port/path)
   - confirmation that WebRTC/SIP over WSS is enabled for your account
   - any required ICE/STUN/TURN settings and supported codecs
4. Android Zoiper's UDP setting cannot be copied directly into a browser PWA.
5. The password is stored in this browser's localStorage if Save Settings is used. Do not save it on a shared device.
6. This is a starter implementation, not a verified integration with your provider. Until the provider supplies WSS/WebRTC details, registration/calls may fail.
