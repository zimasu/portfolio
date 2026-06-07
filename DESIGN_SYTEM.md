## Grid & Spacing
- **Responsive:** Mobile (<768px), Desktop (768px+).
- **Scale:** 8px grid (p-2=8, p-4=16, etc). Stick to this to keep the layout tight.

## Geometry
- **Max Width:** 1100px.
- **Section Height:** `h-[calc(100dvh-72px)]`. (Using dvh for mobile sanity).
- **Navbar:** 72px fixed. Don't use padding-top; use the offset in `handleNav`.

## Typography
- **Headings:** Bebas Neue
- **Body:** DM Sans
- **Meta/UI:** JetBrains Mono
- **Scale:** Keeping it simple with `text-[17px]/relaxed` for body and `text-[11px]/widest` for labels.

## Colors
Defined in `globals.css` via CSS variables:
- **BG:** `#0b0b0d` | **Surface:** `#111115`
- **Text:** Head `#f0f0f5` / Body `#c8c8d8`
- **Accent:** `#10a37f`

## Animation (Framer Motion)
Keep it consistent. All sections use `whileInView` with `-72px` margin.
Stagger elements by `0.1s` per layer:
- **0.0s:** Marker | **0.1s:** Heading | **0.2s:** Body | **0.3s:** Details...

## Structure
- `lib/motion.ts` for shared variants.
- UI components (buttons, etc) go in `components/ui/`.
- Keep section-specific code local to its file to avoid massive imports.
