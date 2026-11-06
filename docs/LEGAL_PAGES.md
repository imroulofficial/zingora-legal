# Legal pages

All legal text is a **draft for review**. Each page shows a draft notice, and every missing fact is
shown as a highlighted `[PLACEHOLDER]`. Have the final text reviewed, ideally by a qualified legal
adviser, before release.

## Information needed from the developer

| Placeholder | Used in | Notes |
|---|---|---|
| Contact email | Privacy, Terms, Support | A monitored address. Also required in Play Console |
| Postal address | Privacy | Required by some laws and by Play for some account types; confirm if needed |
| Effective date | Privacy, Terms | Set when the documents are finalised and published |
| Governing-law jurisdiction | Terms | Usually the country where Red Pen Studio is based |
| Analytics / crash reporting | Privacy | Confirm whether Firebase or any other SDK will be added. The blueprint leaves this open |
| Ad mediation partners | Privacy | None planned. List them if AdMob mediation is added |
| AdMob publisher ID | app-ads.txt | Copy the exact line from AdMob. Never guess it |

## What the Privacy Policy currently states

It reflects the planned v1.0 design (Master Game Blueprint):

- Offline-first, no account, no game server, progress stored only on the device.
- Locally generated installation identifier, progress, settings: never sent to the developer.
- Google AdMob (rewarded and limited interstitial ads, no ads during gameplay, no banners) with
  Google's data processing linked to Google's policies.
- Google UMP consent before ads, with privacy choices available in Settings.
- Audience 13+, not directed at children under 13.

If the app's real behaviour changes (new SDKs, analytics, accounts), the policy **must** be updated
before release. The Play Console Data safety form must match it exactly.
