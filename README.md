# Out There Co. — Landing Page

Single-file HTML landing page for the Out There Co. fishing channel.

## Local preview

Just open `index.html` in a browser. That's it. No build step, no dependencies.

For a slightly better dev experience, run a local server:

```bash
# If you have Python installed
python3 -m http.server 8000

# Or with Node
npx serve
```

Then visit `http://localhost:8000`.

## Before deploying — things to swap in

Search `index.html` for these placeholders and replace them:

1. **Social links** — Find `href="#"` on the YouTube and Instagram buttons (in both the social section and the footer). Replace with your real channel URLs once they exist.

2. **Email signup form** — The Buttondown form currently points to `YOUR_USERNAME`. Once you sign up for a free Buttondown account:
   - Go to Settings → Subscribe Forms
   - Copy your form URL
   - Replace both instances of `YOUR_USERNAME` in the form `action` and `onsubmit` attributes

   If you prefer ConvertKit instead, their embed form goes in the same spot.

3. **Contact email** — The footer has `hello@outtherecompany.com`. Change if you want a different address or if your domain is different.

4. **Coordinates in footer** — Those are Hanson, MA coordinates. Change if you want to use a different location or remove them.

## Deploying to Vercel

1. Create a GitHub account if you don't have one.
2. Create a new repo (e.g. `outthereco-site`). Push this folder to it.
3. Go to vercel.com, sign in with GitHub.
4. Click "Add New Project", pick your repo, hit Deploy. Vercel will give you a URL like `outthereco-site.vercel.app` in about 30 seconds.
5. In Vercel project settings → Domains, add your custom domain.
6. Vercel will give you DNS records to add in Cloudflare. Add them there, and in 5–30 minutes your custom domain will be live.

## Deploying to Netlify

Same process — drag-and-drop or connect a GitHub repo, add your custom domain, update DNS in Cloudflare.

Both Vercel and Netlify are free for a site like this. Vercel's GitHub integration is slightly smoother; Netlify's drag-and-drop is simpler if you don't want to use git.

## Domain note

**Double-check your Cloudflare dashboard for the exact domain spelling.** The email in the footer uses `outtherecompany.com`. If your actual registered domain is different, update the email address accordingly.

## What's next

Once you have real footage:
- Replace the SVG crew portraits with actual photos (swap the `<svg>` inside each `.crew-portrait` for an `<img>` tag)
- Consider adding a section with embedded YouTube videos after Video 1 launches
- Add a "recent trips" or "blog" section if you want to post trip reports
