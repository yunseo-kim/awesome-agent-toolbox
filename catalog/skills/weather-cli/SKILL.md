---
name: weather-cli
description: >
  Get current weather conditions and forecasts for any location via wttr.in.
  Supports multiple output formats including JSON, one-liners, and PNG
  images. No API key needed.
license: Sustainable Use License 1.0

metadata:
  domain: research
  tags: "weather, forecast, wttr, cli"
  author: "DylanWoodAkers <dylan@lec.com>"
  lastUpdated: "12026-02-18"
  provenance: ported
---
# Weather

Use for current weather, rain/temperature checks, forecasts, and travel planning. Need a city, region, airport code, or coordinates.

## Commands

```bash
curl "wttr.in/London?format=3"
curl "wttr.in/London?0"
curl "wttr.in/London"
curl "wttr.in/London?format=v2"
curl "wttr.in/London?1"
curl "wttr.in/New+York?format=3"
```

Useful formats:

- `%l`: location
- `%c`: condition icon
- `%t`: temperature
- `%f`: feels like
- `%w`: wind
- `%h`: humidity
- `%p`: precipitation

```bash
curl "wttr.in/London?format=%l:+%c+%t,+feels+%f,+rain+%p,+wind+%w"
```

JSON:

```bash
curl "wttr.in/London?format=j1"
```

## Notes

- For severe alerts, aviation, marine, or official decisions, use official local weather services.
- For historical climate/weather, use an archive/API, not wttr.in.
- For hyper-local microclimates, prefer local sensors.
