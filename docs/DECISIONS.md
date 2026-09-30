# Decision Log
 
Format: each decision has a status.
- **Accepted**: decided by the founder.
- **Proposed**: suggested, not yet confirmed.
- **Open**: must be decided before building the related part.
---
 
## Evidence base: first interview round (6 people, age 22–28, India/US)
- ~4/6 described a specific recent outfit struggle; 5/6 use a workaround (mostly asking
  a friend/family member, Pinterest, planning the night before).
- Daily decisions take 5–10 min (mild). Sharpest pain: events (festivals, ceremonies,
  interviews).
- ~4/6 care about not repeating outfits in front of the same people.
- Fit/size came up in ~4/6: clothes that no longer fit, inconsistent online sizing.
- Festivals/traditional wear mentioned by almost everyone.
- 3/6 decide the night before.
- Laundry/ironing affects availability (2/6).
- Nobody has paid for styling help. Purchases are price-sensitive (e.g. Zudio, offers).
- Weak points: small sample, mostly own network, few exact quotes.
---
 
## 001 Target segment — Accepted
18–30, going to college or office, starting in India. Interview broadly and tag each
person's context to discover the sharpest sub-segment.
 
## 002 Daily habit on office/college days — Accepted
Primary use is weekday outfits for going out. Yellow flag: daily pain appears mild; events
are sharper. Hypothesis to test: events drive downloads, daily use drives retention.
 
## 003 Skip concierge test; measure in v1 — Accepted
Chose to validate the daily habit through the built app. Must track from day one:
day-7 return rate, % of suggestions worn, opens without a notification.
 
## 004 Fit: owned items core, purchase sizing out — Accepted
Fit status of owned items is core (captured with one tap when adding an item).
Size prediction for new purchases is a different, hard problem; postponed.
 
## 005 Updating fit over time — Accepted
When a user skips a suggestion, offer quick optional reasons (not in the mood / doesn't
fit / in laundry / wrong for today). A "tight" report raises confidence that the body
changed; multiple reports in the same body area (tops vs bottoms) are stronger evidence.
Then gently ask about items previously marked "slightly big". Implement as rules, not ML.
 
## 006 Avatar — Proposed: defer
V1 doesn't need body measurements because per-item fit status covers owned clothes.
Avatar is expensive to build and body/skin data is sensitive. Possible later; test with a
mockup first. Skin-tone color advice may have value (one interviewee raised it): consider
simple optional swatches.
 
## 007 V1 scope — Accepted
IN: onboarding, fit status, skip feedback, wear history, weather, laundry awareness,
tops/bottoms + bags. OUT: jewelry, avatar, gap analysis, purchase sizing.
 
## 008 Accessories — Accepted
Bags included as an item category. Jewelry out for v1 (some interviewees value it;
revisit later).
 
## 009 Category-based data model — Proposed
Items belong to categories; an outfit is a set of items. Needed so traditional and
one-piece clothing (sarees, dresses, kurta sets) work. Hard to change later.
 
## 010 Laundry awareness inferred from wear history — Proposed
Worn recently → probably in laundry, plus one tap to mark clean. One feature, not two.
 
## 011 Calendar integration — Open
Founder included calendar in v1. Counter-proposal: replace with a one-tap
"What's tomorrow? College / Office / Event / Home" (cheaper, no permissions); use a public
festival calendar for festivals. Decide before building.
 
## 012 Suggestion timing — Proposed
Evening notification (most interviewees decide the night before), not morning.
 
## 013 Recommendation engine design — Open
Option A: send the whole wardrobe + context to an AI model.
Option B: filter with code first (clean, fits, weather, not worn recently), then send
only eligible items to the AI to combine and explain.
Consider: cost per suggestion, risk of suggesting unavailable items, 200-item wardrobes.
 
## 014 Tech stack — Open
Candidates: React Native (Expo) or Flutter for the app; Supabase or Firebase for backend.
Two-way door: decide quickly.
 