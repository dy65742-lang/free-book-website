# gayanvardham

A welcoming, responsive library of free public-domain classics. Discover thirteen catalog entries in Hindi, English, Spanish, and French, including all five separately labeled parts of the ancient Indian Panchatantra through title/author search, category filters, and a rotating featured shelf. The built-in reader includes adjustable typography, three reading themes, and pagination. Books also offer TXT downloads and links to Project Gutenberg EPUB editions.

## Technology

TanStack Start, React 19, TypeScript, Vite, Tailwind CSS 4, Lucide icons, and accessible Radix dialogs. Netlify hosts the app and static book assets. Original SVG cover illustrations live in `public/covers`; complete Project Gutenberg text files, including their licenses, live in `public/books`.

## Local development

Use Node.js 22.13 or newer and pnpm:

```sh
pnpm install
pnpm dev
```

The development app runs on port 3000. `pnpm build` produces the production site through the Netlify Vite integration.

## Content

Book texts come from Project Gutenberg and retain their included licenses. The French Monte-Cristo edition is Volume I. EPUB links point to the corresponding Gutenberg edition. Copyright status varies by country. The curated catalog is source-controlled content; the site does not collect user data or persist reader preferences.

Hindi editions contain the five complete parts of Satyakam Vidyalankar’s 1952 Hindi Panchatantra adaptation, sourced from Hindi Wikisource. Each download retains source, translator, and rights information. The Hindi EPUB link exports the entire adaptation from Wikisource; TXT and online reading open the selected part. Hindi search accepts Devanagari and transliterated title/author keywords.

The homepage catalog also includes Gunahon Ka Devta, Bhagavad Gita, October Junction, and Ramayan as four clearly labeled external entries. Gita Supersite provides the Gita reading link; Google Books searches help visitors find editions of the other three titles. These entries do not offer local TXT or EPUB files and are not advertised as hosted free texts. All seventeen entries participate in the combined search and filters; Philosophy is available as a genre filter.
