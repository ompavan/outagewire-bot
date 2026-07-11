# OutageWire-Probe

This page identifies the **OutageWire-Probe** monitoring bot, operated by
Outage Wire (an independent service-status monitor, currently pre-launch).

If you found this page from a `User-Agent` in your server logs, it looked
like this:

    OutageWire-Probe/1.0 (+https://github.com/ompavan/outagewire-bot)

## What it does

- Checks the public availability of a small, fixed list of well-known
  services. **While the service is pre-launch, the probe only contacts
  domains we operate ourselves.**
- Polite by design: a fixed cadence of roughly **one request per minute per
  region per target** — a single `HEAD` or one small `GET`, never page
  asset chains, never crawling, no simultaneous bursts across regions.
- Honors `robots.txt` (match it under the token `OutageWire-Probe`) and
  `Retry-After` headers.

## How to opt out

- Add a `robots.txt` rule for `User-agent: OutageWire-Probe` — the probe
  checks and obeys it.
- Or email us (below); a removal request is honored permanently.

## Contact

Abuse or questions: **abuse@outagewire.com**

This interim page will be replaced by `https://outagewire.com/bot` when the
service launches; the link in the User-Agent will follow.
