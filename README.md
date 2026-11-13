# Dinner Picker 🍽️

Tinder for dinner. You and your partner swipe on restaurants around Radford, Fairlawn and Christiansburg, VA. When you both swipe right on the same place, that's where you eat.

## How to use it

**Swiping together (live):**
1. One person taps **Start a session**, picks the area, radius and kinds of places, and taps **Find restaurants**.
2. A 5-letter room code appears. The other person enters it (or opens the invite link).
3. You both swipe through the same cards on your own phones. As soon as you both like the same place, both phones show **It's a Match!**

**Not at the same time:** tap *"Swipe first and text them a link"*. When you're done, send the link. Your partner swipes the same cards, and they get a match when they like a place you liked.

At the end you see all your matches. You can pick one, or tap **Let fate decide**.

## How it works

- Restaurants come live from **OpenStreetMap** (Overpass API), so the list stays current and there are no API keys. If a place is missing or wrong, anyone can fix it at openstreetmap.org.
- The two phones sync directly (peer to peer, WebRTC via PeerJS). There's no server and no accounts.
- It's three static files (`index.html`, `style.css`, `app.js`), so it runs on GitHub Pages.

## Putting it online (GitHub Pages)

1. In this repo, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick `main` and `/ (root)`, and click **Save**.
3. After a minute or two it's live at **https://chapmanrackaway.github.io/dinnerpicker/**

Add it to your phone's home screen (Share → *Add to Home Screen*) and it behaves like an app.

## Changing the default areas

The town presets (center point and default radius) are in the `AREAS` list at the top of `app.js`. Add a line there and a matching `<option>` in `index.html` to add another town.

## Running locally

Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
