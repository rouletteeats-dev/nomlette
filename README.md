# nomlette — your website folder

**Dinner, decided.** A Melbourne spin-to-decide food and drink site.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The whole website. This is the main file. |
| `spots.json` | The list of places. This is the file you replace when you add or edit spots. |
| `logo.svg` | Your logo, traced as a sharp vector. The site recolours it cream. |
| `favicon-32.png`, `apple-touch-icon.png` | The little icon in the browser tab and on a phone's home screen. |
| `og-image.png` | The picture that shows when someone shares your link (Instagram, iMessage, WhatsApp). |
| `img/` | The eight mood photos used in the big sections. Upload this folder too. To swap a photo, upload a new one with the same file name. |

Colours: cream `#FFF3EA`, brown `#874C23`, olive `#6F6A30`, dusty blue `#4D6B94`, deep brown `#24160E`. Headline font: Noto Serif Display (extra condensed). Body font: Inter.

## Put it online (free, about 10 minutes)

**Vercel (easiest)**
1. Make a free account at github.com. Click **New repository**, name it `nomlette`, keep it **Public**, click **Create**.
2. On the new repository page click **uploading an existing file**. Drag in everything from this folder, including the `photos` folder, then click **Commit changes**.
3. Go to vercel.com and sign up with GitHub. Click **Add New → Project**, pick `nomlette`, click **Deploy**. You don't need to change any settings.
4. You get a link like `nomlette.vercel.app`. From now on, every time you upload a changed file to GitHub the site updates by itself in a minute or two.

**GitHub Pages (alternative)**: in the repository go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**. Your link appears after a minute.

## Add or edit spots

1. Scroll to the very bottom of the site and click **Owner tools**.
2. Click **Add a spot**, or click any spot in the list to edit it. Click **Save**. At this point the change only exists in your own browser.
3. When you're happy, click **Download spots.json**.
4. On GitHub open your repository, click **Add file → Upload files**, drag in the new `spots.json` (same name, so it replaces the old one) and click **Commit changes**. The live site updates in a minute or two.

Useful buttons in Owner tools: **Back up my changes** and **Restore a backup** keep a safety copy of your edits, and **Undo all my changes** goes back to the published list.

## Photos

I did not pull photos from Google Images. They belong to the photographers and venues, using them on a public site can lead to takedown notices, and I can't guarantee a search result is actually that venue. Instead every spot has a photo slot. Until one is filled, the card shows a colour tile with the cuisine in large type, so the site never looks broken.

**To add a photo**
1. Save the photo as a JPG with a simple name, for example `lune.jpg`, ideally under 300 KB (squoosh.app shrinks them). On GitHub click **Add file → Upload files**, drag the photo in and click **Commit changes**.
2. In **Owner tools**, open the spot and type the file name, `lune.jpg`, into **Photo web address**. Put a credit such as `Photo: Lune Croissanterie` into **Photo credit**. (You can also paste a full `https://` address of a photo you have permission to use.)
3. Click **Save**, then **Download spots.json**, then upload it as above.

**Where to get photos you're allowed to use**
- Ask the venue. A short Instagram DM works: "Can we use one of your photos on nomlette with a credit?" Most small venues say yes.
- Your own photos from visits.
- Free stock sites (Unsplash, Pexels) only for general atmosphere, never as "the" photo of a real venue.
- Later, if you want photos for every spot automatically: the Google Places API provides official place photos with required attribution. It needs a Google Cloud account with billing and a little code, so ask me when you're ready.

## Small settings

Open `index.html` in any text editor (or click the pencil icon on GitHub) and use Find:
- `CONTACT_URL`: put a form link or a `mailto:` address between the quote marks to show **Suggest a spot** in the footer.
- `INSTAGRAM_URL`: paste your Instagram link to show **Instagram** in the footer.
- `og-image.png` (appears twice): once you know your live address, replace it with the full address, for example `https://nomlette.vercel.app/og-image.png`, so link previews show your logo.

## Good to know

- Hours and prices are estimates. The site says **Likely open**, not **Open**. Please check and correct them in Owner tools.
- Map pins are approximate, placed around each suburb. Every spot has **Get directions**, which opens Google Maps for the exact place. For an exact pin, add Latitude and Longitude in Owner tools (on desktop Google Maps, right-click the place and click the numbers to copy them).
- **Hidden gem**, **Viral** and **Boozy brunch** are my editorial picks. Change them in Owner tools as you see fit. Boozy brunch is deliberately a short list.
- Ratings are left out on purpose, because I couldn't verify them.
- Map tiles come from CARTO and OpenStreetMap, free for small sites with the credit shown on the map. If the site gets very busy you'll need a tile plan.
- Everything is tested with 86 automated checks, but the real map and Google Fonts couldn't load in my test environment. Click through the live site once after you deploy.
