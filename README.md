# Sunvel Exports — Cinematic Corporate Website

A four-page React/Vite website for **Sunvel Exports** with a cinematic, tactile design language combining glassmorphism, restrained neumorphism, skeuomorphic material cues, GSAP scroll motion, and a Three.js pointer-reactive hero globe.

## Pages
- Home
- Products
- Gallery
- Contact Us

## Key interactions
- Cinematic looping hero video with poster fallback
- Three.js wireframe trade globe reacting to pointer position
- GSAP scroll reveals and parallax
- Custom cursor on fine-pointer devices
- 3D tilt + cursor lighting on cards
- Responsive catalogue search/filtering
- Editorial gallery filtering + lightbox
- Product-specific enquiry links
- Real `/api/contact` serverless handler (Resend). The UI reports success only after the provider accepts the email.
- Reduced-motion and touchscreen fallbacks

## Important content note
The supplied brief explicitly says not to fabricate products, certifications, export destinations, statistics, testimonials, or contact details. Since a verified Sunvel product catalogue and verified public contact details were not supplied for this build, the product cards are intentionally marked placeholders and the site does not publish an invented phone/email/address.

Replace `src/data/catalog.js` with verified products and swap the stock gallery images for Sunvel's real imagery when available.

## Setup
```bash
npm install
npm run dev
```

## Production build
```bash
npm run build
npm run preview
```

## Contact form configuration (Vercel + Resend)
Create environment variables using `.env.example`:
- `RESEND_API_KEY`
- `CONTACT_TO_EMAIL` — verified Sunvel recipient email
- `CONTACT_FROM_EMAIL` — a sender/domain allowed by Resend

Deploy to Vercel. The contact form posts to `/api/contact`. If the variables are missing, the API returns a visible configuration error; it does not fake success.

## Visual asset sources used in this prototype
These are external URLs so the repository remains lightweight. Replace them with optimized local WebP/AVIF/MP4 assets for final production if preferred.

- Hero video: Pexels, Glenn Langhorst — “Aerial view of a container ship at a commercial dock, highlighting freight transportation.”
  https://www.pexels.com/video/filled-with-containers-ship-in-commercial-dock-10458151/
- Port imagery: Unsplash, PortCalls Asia — cargo ship at port
  https://unsplash.com/photos/_FLuF7RYZ1E
- Port imagery: Unsplash, Daniel Miksha — container ship at Vancouver port
  https://unsplash.com/photos/4ZornyPnGlA
- Port imagery: Unsplash, Haris Illahi — cargo ships at busy port
  https://unsplash.com/photos/HqYPlDuAyBE
- Air cargo imagery: Unsplash, Sevcan Alkan — cargo containers inside aircraft
  https://unsplash.com/photos/D1H7jEwlWMU

Review each provider's current license/attribution requirements before commercial launch.

## Design research basis
The interaction system was informed by current cinematic-web patterns: scroll-driven narratives, pinned progression, clip/image reveals, WebGL depth, pointer-responsive elements, and performance-conscious reduced-motion fallbacks. It is an original Sunvel implementation rather than a copy of any one reference site.
