# Design Document - Authentic-AI Content Hub

## 1. Architecture Overview
The application follows a modern Frontend-heavy architecture using Next.js (App Router) for performance and SEO.

## 2. Tech Stack
- **Framework:** Next.js 15
- **Styling:** Tailwind CSS (Theme: Organic Tech / Ghibli-inspired)
- **Animations:** Framer Motion
- **Libraries:** ExifReader (Metadata parsing), Lucide-React (Icons)

## 3. Component Hierarchy
- `Layout`: Main wrapper with navigation and Ghibli-inspired background.
- `UploadZone`: Interactive drag-and-drop area using React-Dropzone.
- `TrustDashboard`: Main container for results.
    - `VerificationGauge`: Visual score (0-100% human-made).
    - `NutritionLabel`: Detailed breakdown of content "ingredients."
    - `TimelineView`: Vertical stepper for file history.
- `ExportBadge`: Generates a shareable "Verified by Authentic-AI" JSON-LD snippet.

## 4. Data Flow
1. User uploads file via `UploadZone`.
2. Client-side logic uses `ExifReader` to parse binary data.
3. Metadata is compared against known AI signatures (Midjourney, DALL-E) and C2PA standards.
4. `TrustDashboard` state updates to reflect the findings.
