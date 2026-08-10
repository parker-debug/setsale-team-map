# SetSale — Meet the Team

Interactive team map + directory. Single static page, no build step.

## Files

```
index.html      the whole page (HTML, CSS, JS, and team data)
photos/         headshots, one PNG per person
```

## Adding or editing a person

Open `index.html`, scroll to `const teamMembers = [`, and copy an existing block:

```js
{
  name:      "First Last",
  title:     "Job Title",
  location:  "City, ST",
  latitude:  39.9612,
  longitude: -82.9988,
  photo:     "photos/FirstName.png",
  bio:       "One or two sentences."
},
```

- Drop the headshot in `photos/` with a matching filename.
- Get lat/long from Google Maps: right-click the location, click the coordinates to copy.
- If two people share a city, nudge one set of coordinates by ~0.02 so the map pins don't stack.

## Mapbox

The map uses a public Mapbox token (`pk.…`) near the top of the `<script>` block. Public
tokens are meant to be exposed in client-side code, but restrict it to your GitHub Pages
URL under Mapbox → Account → Tokens → URL restrictions.
