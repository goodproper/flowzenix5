# FlowZenix Portfolio

A responsive static portfolio built with plain HTML, CSS, and JavaScript. There is no build step or package dependency.

## Files

- `index.html` — page content, styling, and small mobile navigation script.
- `flowzenix-logo.jpg` — supplied full FlowZenix logo used in the About section.
- `logo-mark.png` — cropped logo emblem used in the header and favicon.
- `social-preview.png` — Open Graph and Twitter sharing image (1200 × 630).
- `thank-you.html` — destination after a successful Netlify form submission.

## Contact configuration

The portfolio currently uses the provided contact details:

- Email: `flowzenix.digital9@gmail.com`
- WhatsApp: `+91 91365 87600`

The WhatsApp link opens a new chat with a prefilled message. Confirm these details before publishing if they have changed.

The contact form uses Netlify Forms (`data-netlify="true"`) with a honeypot field and browser-required validation. It does not pretend to submit from a local file preview. Before it can accept submissions, enable form detection in the Netlify site's Forms settings, deploy this version, confirm a `project-enquiry` form appears in the Forms dashboard, and configure a notification recipient there. Submit a real test enquiry and check that it appears in Netlify and reaches the configured notification inbox before relying on it. Netlify provides its own error response if a submission fails; the thank-you page is reached only after successful submission. See [Netlify's form setup](https://docs.netlify.com/manage/forms/setup/) and [spam filter documentation](https://docs.netlify.com/manage/forms/spam-filters/).

## SEO and social sharing

The canonical URL, Open Graph URL, and image URLs in `index.html` use `https://flowzenix9.netlify.app/`. Update them if the deployed site uses a different domain. Netlify serves the assets from the site root. The social preview should be checked with the target platforms after deployment.

## Project information

The three demo project sources were not included in this archive. Project cards describe them as concepts and avoid unverified technical claims. The portfolio artwork is illustrative, not a screenshot of those projects.

The café demo's existing URL still contains `dummycafepage`; its source was not supplied, so this portfolio cannot change the branding on that external site.

## Run locally

From this project folder, run `python -m http.server 8000` and open `http://localhost:8000/`. No install or build command is required. The form is handled only by Netlify after deployment; a local preview cannot submit enquiries.

## Deploy to Netlify

1. Deploy the folder containing `index.html`, `logo-mark.png`, `flowzenix-logo.jpg`, and `social-preview.png` to the existing Netlify site (or connect the folder's repository).
2. Use no build command and set the publish directory to the project root, where `index.html` is located.
3. Confirm the site URL matches the canonical and social metadata, then test the deployed links and contact actions.
4. If deploying under a custom domain, update the canonical, Open Graph, and Twitter image URLs in `index.html`.

Netlify does not require a redirect configuration for this single-page static site.


Simple Apps Script setup: this static version posts enquiry fields directly to the configured Apps Script URL and displays a success popup after the browser request completes. Because Apps Script cross-origin responses cannot be read in no-cors mode, verify the first test submission in Google Sheets.
