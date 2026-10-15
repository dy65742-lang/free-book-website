# Project guide

gayanvardham is a free multilingual classics library built with TanStack Start, React, TypeScript, and Tailwind CSS. The design uses warm paper colors, muted green, DM Sans interface typography, and Libre Caslon Display headings.

## Architecture

- `src/routes/index.tsx`: home page, curated catalog, search, genre/language filters, featured shelf, about dialog, and full-text reader.
- `src/routes/__root.tsx`: document shell, social metadata, tooltip and toast providers.
- `src/styles.css`: theme variables, responsive layouts, cover arrangements, and reader themes.
- `public/covers/`: original SVG illustrations. Cover filenames match Gutenberg book IDs or the Hindi Panchatantra part identifiers.
- `public/books/`: complete UTF-8 book texts with original Gutenberg license notices or Hindi Wikisource source and rights attribution. Reader fetches these same-origin static assets on demand.
- `src/components/ui/`: reusable accessible Radix-based components.
- `vite.config.ts`, `netlify.toml`: TanStack and Netlify integration.

## Conventions and decisions

Use typed React components and hooks. Keep the catalog metadata aligned with its text and cover assets. Preserve the Gutenberg license notices in all downloadable files. The French edition is explicitly Volume I, not the complete multi-volume work. Online reading removes the introductory Gutenberg header for comfort but retains the original downloaded file. EPUB links use Gutenberg for Gutenberg editions and Wikisource export for the full Hindi Panchatantra adaptation; each Hindi catalog entry contains one complete part.

Search and filters combine; clearing filters restores every book. Reader settings and page selection are transient UI state. No accounts, database, analytics, or saved reading history are implemented. Any future persistent user data must use Netlify platform storage.

Keep icon controls labeled, keyboard focus visible, dialogs accessible, motion respectful of reduced-motion preferences, and layouts usable on small screens. Use existing Radix dialog components for overlays. Route types are generated automatically; do not edit the generated route tree.

## Working on this project

Install with `pnpm install`, run locally with `pnpm dev`, and build with `pnpm build`. During automated Netlify agent runs, follow the run instructions: validation occurs in the platform pipeline, so do not start local build, test, or development processes.
