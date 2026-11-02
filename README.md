# Stripeshow landing page

A one-page site for Stripeshow, a heated, walk-in driving range planned for Utah County, aimed at UVU and BYU students. It's plain HTML and CSS with no build step, made to be hosted on GitHub Pages.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole page: pitch, the winter-practice problem, features, pricing, a 6-question student survey (short version of PRD Appendix A), and an email signup. |
| `style.css` | All styling. Brand colors live in the `:root` block at the top. |

## Setting up the forms (one-time)

GitHub Pages only serves static files, so the survey and email signup send their responses to [Formspree](https://formspree.io) (the free plan covers 50 submissions a month).

1. Create a free Formspree account and a new form.
2. Copy its ID (the part after `/f/` in the endpoint, e.g. `xyzabcde`).
3. In `index.html`, replace both instances of `YOUR_FORM_ID` with that ID.

Both forms send to the same inbox. Each submission has a `form` field set to `survey` or `signup`, plus its own email subject line, so you can tell them apart and export them separately as CSV.

## Publishing on GitHub Pages

1. Push this folder to a public GitHub repo.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Previewing locally

Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
