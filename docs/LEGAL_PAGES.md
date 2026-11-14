# Legal pages

All placeholders were filled on November 8, 2026 (Phase I). The Privacy Policy and the Terms &
Conditions are in effect from that date. Having the text reviewed by a qualified legal adviser is
still recommended.

## Values used

| Detail | Value | Used in |
|---|---|---|
| Effective date | Privacy: November 14, 2026 (Meta added Nov 13; US opt-out turns Meta off and "no analytics of how you play" wording Nov 14); Terms: November 8, 2026 | Privacy, Terms |
| Contact email | mdimroulhassanofficial@gmail.com | Privacy, Terms, Support |
| Postal address | North Jaldi, Post Office: Jaldi - 4390, Banshkhali, Banshkhali Municipality, Chittagong, Bangladesh | Privacy, Terms, Support |
| Governing law | Bangladesh, without limiting mandatory consumer-protection and privacy rights under the user's own law | Terms |
| Developer | Red Pen Studio | All pages |
| Analytics / crash reporting | None. The app contains no analytics SDK (owner decision) | Privacy |
| Ad networks | Google AdMob only, no mediation partners | Privacy |
| Ad measurement | Meta (Facebook) SDK core: install and app-open events for app install ads, only when consent allows; Limited Data Use for US states (added November 13, 2026); a US-state opt-out of sale/sharing or targeted ads turns Meta off (November 14, 2026) | Privacy section 6 |
| AdMob publisher ID | pub-1848535996024012 | app-ads.txt |

## What the Privacy Policy states

It reflects the app as built (Phase I):

- Offline-first, no account or login, no game server, progress stored only on the device.
- Locally generated installation identifier, progress, settings, ad frequency records and the UMP
  consent choice: stored on the device, never sent to the developer.
- No analytics or crash-reporting SDK.
- Google AdMob (optional rewarded ads and occasional full-screen ads after a won level; none in levels
  1-12, at start, during play or after a loss; no banners), advertising ID, links to Google's policies.
- Ad requests are not child-directed and limited to teen-rated content (max ad content rating T).
- Google UMP consent before any ad request; Settings > Privacy & Ad Preferences to change it.
- Meta (Facebook) install measurement (section 6, November 13, 2026): what Meta receives (install and
  open events, advertising ID, Meta's app ID, IP / approximate location, device and app info, install
  referrer, SDK diagnostics), why (measuring app install ads), the consent rules per region, Limited
  Data Use, links to Meta's policies, and how to opt out.
- Audience 13+, not directed at children under 13.
- Data deletion by uninstalling or clearing the app's storage.

## Keep the app in step

The app embeds byte-for-byte copies of `privacy-policy.html` and `terms-and-conditions.html` for its
offline viewer. If you change either page, copy it into the game repository at
`app/src/main/assets/legal/` in the same release. The Play Console Data safety form must also match
the policy.
