# AGENTS.md — Trip Itineraries Wiki

Guidelines for managing, structuring, creating, and maintaining pages within
`wiki/trip-itineraries/` and its subdirectories.

---

## Directory Structure

```
wiki/trip-itineraries/
├── AGENTS.md               ← this file
├── index.md                ← root index, links to all destination directories
└── <destination>/          ← e.g. japan/
    ├── index.md            ← destination index, links to all city directories
    └── <city>/             ← e.g. tokyo/, osaka/, kyoto/
        ├── index.md        ← city index, lists all day-trip pages
        ├── <trip-name>.md  ← general day-trip page
        └── <YYYY-MM-DD-trip-name>.md  ← date-specific event page
```

Every directory **must** contain an `index.md`. No pages should exist outside
this hierarchy without a corresponding entry in their parent `index.md`.

---

## File Naming

### General day-trip pages

Use a short, lowercase, hyphen-separated description of the trip theme.

```
akihabara-maid-cafes-and-retro-gaming.md
dotonbori-food-and-nightlife.md
arashiyama-bamboo-and-temples.md
```

### Date-specific event pages

Prefix the filename with the event's start date in `YYYY-MM-DD` format,
followed by a short description.

```
2026-05-20-tokyo-port-festival.md
2026-06-01-kifune-matsuri.md
```

Use the **first day** of the event as the date prefix even if it spans
multiple days.

---

## Page Templates

### General Day-Trip Page

```markdown
# <Title>

**City:** <City name>
**Best for:** <Comma-separated interests, e.g. food, maid cafes, onsen>
**Approximate duration:** <Half day / Full day> (<N–N hours>)
**Estimated cost:** <¥X,000–¥Y,000> (<brief cost note>)

---

## Overview

<2–4 sentence description of the trip. What makes it special, the overall
mood/pace, and what the visitor can expect.>

---

## Itinerary

🗺️ [Get transit directions from your accommodation to <First Stop Name>](<Google Maps URL: destination only, travelmode=transit>)

### <Time of day> — <Stop name> (<HH:MM>)

[![<Alt text>](<DIRECT_IMAGE_URL>)](<SOURCE_PAGE_URL> "<Alt text>")

**📍 <Address or area>**

<Description of the stop: what to do, what to see, what to eat/drink, how
long to spend, and estimated budget for this stop.>

🗺️ [Directions to <Next Stop Name> (<transport mode, ~N min>)](<Google Maps URL: origin + destination, travelmode=transit>)

### <Next stop> ...

🗺️ [Get transit directions from <Last Stop Name> to your accommodation](<Google Maps URL: origin only, travelmode=transit>)

---

## Tips

- <Practical tip>
- <Practical tip>
- <Practical tip>
```

### Date-Specific Event Page

```markdown
# <YYYY-MM-DD>: <Event Name>

**City:** <City name>
**Venue:** <Venue name and area>
**Date:** <Full date(s), e.g. May 20, 2026>
**Hours:** <HH:MM–HH:MM> (or "check official site")
**Tickets:** <¥X,000 / Free / Lottery>
**Ticket URL:** <URL>  ← omit if no URL available

---

## Overview

<2–4 sentence description of the event. What it is, why it matters, and what
the experience is like.>

> **Date-specific:** <One-line reminder of the date(s) and any booking
> requirement.>

---

## Itinerary

🗺️ [Get transit directions from your accommodation to <First Stop Name>](<Google Maps URL: destination only, travelmode=transit>)

### <Time of day> — <Stop name> (<HH:MM>)

[![<Alt text>](<DIRECT_IMAGE_URL>)](<SOURCE_PAGE_URL> "<Alt text>")

**📍 <Address or area>**

<Same stop format as general pages, adjusted for the event structure.
Include pre-event and post-event suggestions where relevant.
Add a 🗺️ transit directions link between each stop, and after the last stop
a link for the user to find their own route back to their accommodation.>

🗺️ [Get transit directions from <Last Stop Name> to your accommodation](<Google Maps URL: origin only, travelmode=transit>)

---

## Tips

- <Practical tip>
- <Practical tip>
```

---

## Index Page Templates

### City Index (`<city>/index.md`)

```markdown
# <City>: Day-Trip Itineraries

**Stay dates:** <Month DD–DD, YYYY>
**City overview:** <2–3 sentence description of the city's character and
highlights relevant to the trip.>

---

## General Day Trips

These itineraries can be done on any day during the <City> stay
(<date range>):

| Page | Description |
|------|-------------|
| [<Title>](<filename>.md) | <One-line description> |

---

## Date-Specific Events

These day trips are tied to specific dates:

| Page | Date | Description |
|------|------|-------------|
| [<Title>](<YYYY-MM-DD-filename>.md) | <Month DD (–DD)> | <One-line description> |

---

## Notes

- <Any important caveats, booking requirements, or scheduling advice>
```

### Destination Index (`<destination>/index.md`)

```markdown
# <Destination> Trip Itineraries

**Trip:** <Trip name>
**Dates:** <Full date range>

---

## Cities

| City | Stay Dates | Index |
|------|-----------|-------|
| <City> | <dates> | [<City> Itineraries](<city>/index.md) |

---

## Trip Overview

<Short paragraph describing the overall trip arc.>

## Key Interests Covered

| Interest | Where |
|----------|--------|
| <Interest> | <City / specific pages> |
```

### Root Index (`index.md`)

```markdown
# Trip Itineraries Wiki

<One-line welcome sentence.>

---

## Destinations

| Destination | Index |
|-------------|-------|
| <Destination> | [<Destination> Itineraries](<destination>/index.md) |

---

## How to Use This Wiki

<Brief explanation of general vs date-specific pages and the naming
convention.>
```

---

## Content Rules

### Language

All content must be written in **English**.

### Data sourcing

All POI details, event names, dates, prices, addresses, and URLs must be
sourced from the **trip planning graph** as the primary source. Use web
research (`browse-web` skill) only when required information is genuinely
absent from the graph.

### Trip design

- Every day trip must be completable in **one day** without feeling rushed.
- Aim for **3–6 stops** per itinerary. Fewer stops with adequate time at each
  is better than a packed schedule.
- Include **estimated costs** per stop and in the metadata header.
- Include a **📍 address or area** line under each stop heading.
- End each page with a **Tips** section (3–5 bullet points) covering practical
  advice: transport, booking requirements, best times, cash vs card, etc.

### Date-specific events

- A page is date-specific when the event is **bound to specific calendar
  dates** and cannot simply be rescheduled by the visitor.
- Date-specific pages must include a `> **Date-specific:**` blockquote in the
  Overview section summarising the dates and any advance booking requirement.
- Date-specific pages do **not** count toward the minimum two general
  day-trips per city per day.

### Images

Every stop must include exactly one image, with the following exceptions:

- **Transit stops** (e.g. walking to or from a railway station, or
  walking/driving between stops) do **not** require an image unless there
  is something notable to see along the way.
- **Do not re-use the same image** on the same page more than once.
- If no appropriate image can be found on Wikimedia Commons (step 4 below),
  **omit the image entirely** for that stop rather than using an unsuitable
  one.

These rules apply to both General Day-Trip Pages and Date-Specific Event Pages.

Place the image immediately after the
`### <Time of day> — <Stop name> (<HH:MM>)` heading and before the
`**📍 <Address or area>**` line. Images are displayed inline and link to
their original source using this format:

```markdown
[![<Alt text>](<DIRECT_IMAGE_URL>)](<SOURCE_PAGE_URL> "<Alt text>")
```

**Do not save images locally.** All images must reference remote URLs.

Image source priority (use the first source that yields a suitable result):

1. **Official event/venue website** — press images or OGP images from the
   event's own site
2. **Trip blogs or news articles** — photos from the actual event or location
3. Search on https://duckduckgo.com/ — Get the images from the target page, not
   from the thumbnail overview. Click on the search result and open the target
   page to retrieve the image from there. If you are unsuccessful, try up to 3
   different queries before giving up.
4. **Wikimedia Commons** — only as a last resort, after at least 3 failed
   DuckDuckGo attempts. NEVER directly start with Wikimedia Commons right away
   before attempting the higher priority sources.

Only use images that are publicly accessible without login. Make sure that you
don't add images that don't load. Images MUST be smaller than 5 MB.

### Google Maps links

Every itinerary page must include Google Maps transit direction links:

- **Before the first POI:** a link with only the `destination` set (no origin),
  so the user can enter their own starting point:
  `https://www.google.com/maps/dir/?api=1&destination=<encoded+name+and+address>&travelmode=transit`
- **Between each pair of consecutive stops:** a link with both `origin` and
  `destination` set:
  `https://www.google.com/maps/dir/?api=1&origin=<encoded>&destination=<encoded>&travelmode=transit`
- **After the last POI:** a link with only the `origin` set (no destination), so
  the user can enter their own accommodation:
  `https://www.google.com/maps/dir/?api=1&origin=<encoded+name+and+address>&travelmode=transit`

Label each link with a 🗺️ emoji and a short human-readable description including
the expected transport mode and approximate travel time where known, e.g.:
`🗺️ [Directions to Nakano Broadway (JR Chuo Line, ~20 min)](…)`

### Uniqueness

No two day-trip pages in the same city should cover the same primary POIs in
the same order. Overlap between pages is acceptable (e.g. ending different
trips in Dotonbori) but each page must offer a distinct experience.

---

## Index Maintenance

Whenever a page is added, removed, or renamed:

1. Update the **city `index.md`** — add/remove/update the row in the
   appropriate table (General Day Trips or Date-Specific Events).
2. Check that the **destination `index.md`** does not need updating (it links
   to city indexes, not individual pages — only update if a city is
   added/removed).
3. Check that the **root `index.md`** does not need updating (it links to
   destination indexes only).

Never leave a page without a corresponding index entry, and never leave an
index entry pointing to a non-existent file.

---

## Adding a New City or Destination

1. Create the directory: `wiki/trip-itineraries/<destination>/<city>/`
2. Create `index.md` in the new city directory using the city index template.
3. Create at least **two general day-trip pages** to start.
4. Add the city to the destination `index.md`.
5. If adding a new destination entirely, also create a destination `index.md`
   and add an entry to the root `index.md`.
