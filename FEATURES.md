# Song Requests App — Feature List

## 🎤 Audience Experience

- Browse the setlist grouped by genre, in collapsible sections
- Search by song title and artist in separate fields, with typo-tolerant fuzzy matching
- Songs sort by all-time popularity — the songs people have asked for most across every gig float to the top
- "Sorry, I don't know that one!" message when a search comes up empty
- Request a song with an optional name and note
- **Happy Birthday special flow**: choose "Sing next" or "Sing later" (with a "when?" field and example suggestions), a custom note prompt for the birthday message, the requester's name is shown publicly for birthday songs only — every other request stays anonymous to the crowd
- Duplicate requests bump the existing entry's counter and push it up the queue instead of duplicating it
- A person can't request the exact same pending song twice, but others can still pile on
- 15-minute cooldown before a played song can be requested again
- Max 10 pending requests in the queue at once (drops to 5 during Last Call)
- Max 4 active requests per person at a time
- **Save-for-later heart** — during a break only, tap ♥ to queue a song without opening the full request form
- Live "Up Next" queue visible to the audience, separate from browsing
- Optional "vibe" tag shown on songs (e.g. Acoustic, Dance)
- Songs marked "not tonight" by the host are hidden automatically
- Status banner: Taking requests / On a break (with live countdown) / Done for the night / Not started yet
- Last Call banner
- Custom banner image support
- "Hello! Welcome to [venue] — You are listening to [band]" message
- Follow-me and Follow-my-band buttons showing the actual @handle, open directly
- Tip the band button
- 🔥 Fire reactions on the currently playing song — unlimited taps, live shared count
- Confirmation and limit messages appear as a centered popup, not a corner toast

## 🎛️ Running a Session (Host)

- PIN-protected dashboard login
- Start a session: optional venue name, pick which setlist to run if you have more than one
- Warning if starting a new session would overwrite an unplayed leftover queue
- End session (with a confirmation prompt) → generates a stats recap and clears the queue automatically
- Pause requests with quick presets (5/10/15/30 min) **or** "Done for tonight" (indefinite), each with a Back option
- Last Call toggle: flashes a banner to the audience and drops the queue cap to 5
- Live break countdown shown on both the audience screen and your own dashboard
- One-tap song lifecycle — mark a song "Play now" and whatever was previously playing is automatically marked finished; a "Finished" button appears on its own only when the queue would otherwise get stuck with nothing else to press
- Played-song history with auto-clear after 3 hours (toggleable)
- Silent vibration alert on new requests (no sound), toggleable

## 🎵 Setlist Management

- Multiple named setlists — switch, duplicate, rename, or delete (always keeps at least one)
- CSV upload: replace or add-to-current-list, auto-detects title/artist/genre/vibe columns
- Manual add, edit, and remove songs
- Mark songs "unavailable" for tonight without deleting them from the list

## 📊 Stats & History

- End-of-session recap: total requests, songs searched-but-missing (with one-tap "add to setlist"), crowd favorites by fire count, requests-per-hour pace, named-vs-anonymous split, birthday count
- History tab: every past session, expandable for full detail, each with its own "add to setlist" button for anything searched but missing that night; delete individual sessions or clear all
- All-time stats, shown as collapsible sections: Top 10 all-time requests, crowd favorites, "Hidden gems" (high fire-to-request ratio), songs never requested, breakdown by genre, breakdown by venue, your single busiest gig

## 🔒 Security

- PIN required for all dashboard access
- Wrong PIN guesses and wrong security-question answers trigger an escalating lockout (1 minute, then 5, 15, and finally an hour per wrong guess)
- Up to 3 custom security questions, one asked at random for PIN recovery — no upfront hints, no self-service bypass

## 🎨 Personalization

- 9 themes: Original, Retro Future, Dark, Light, Sunset Lounge, Vinyl, Forest Folk, High Contrast, Festival
- Theme picker as a collapsible dropdown with live swatch previews

## ⚙️ Settings

- Band name, personal Instagram, band Instagram, tip link, banner image, PIN — each field shows its current value and saves exactly what's typed

## 🛠️ Technical

- Real-time sync across every device via Firebase/Firestore
- Deployed on GitHub Pages, built automatically by GitHub Actions — no local terminal needed
- Tailwind CSS configured for production
