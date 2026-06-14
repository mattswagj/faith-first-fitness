# Faith First Fitness — Website

A bright, kid-energetic one-page site for **Faith First Fitness** (Coach Lucas & Fun Freddie).

## Files
- `index.html` — the entire website (HTML, CSS, JS in one file). Static, deploys anywhere.

## Brand
- Tagline: **"I Can Do It! Fun Children Fitness!"**
- Colors: navy `#16164a` + rainbow accents (red/orange/yellow/green/blue/purple/pink)
- Fonts: Baloo 2 + Fredoka (headings), Nunito (body)
- Mascot: **Fun Freddie** the bunny

## Swapping in the real logo / photos
- The logo is currently a hand-drawn SVG placeholder in the nav (and a matching mascot in the hero & Fun Freddie sections).
- To use the real logo: in `index.html`, find the comment `LOGO: swap this <svg>...` in the nav and replace the `<svg>...</svg>` with `<img src="logo.png" alt="Faith First Fitness" style="height:54px">` (drop `logo.png` in this folder).
- Send photos anytime and they can replace the SVG mascots / fill a photo gallery.

## Contact form → Supabase
- Submissions save to Supabase project **faith-first-fitness** (`alebrgmhuemsvcjdiqth`), table `public.leads`.
- The form uses the public **anon** key (safe to expose — that's by design).
- Row-Level Security: anonymous visitors can **insert only**. No one can read submissions with the public key.
- **View your leads:** Supabase dashboard → Table Editor → `leads`.
- Note: a public form can receive spam. If that becomes an issue, add a captcha (e.g. hCaptcha/Turnstile) or basic rate limiting.

## Columns in `leads`
`id, created_at, name, email, phone, child_age, interest, message`

## Deploy
Deployed as a static site on Vercel. Re-deploy after edits to publish changes.
