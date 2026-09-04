## v0.1.43

- Import net daily cost into recorder long-term statistics via the Recent Cost Total sensor, so it can be paired with the Recent Usage Total statistic as the Energy Dashboard's grid consumption cost stat. Daily resolution only, since GloBird does not publish half-hourly cost detail.
- Confirm and document that statistics imports are additive only: every sync upserts the currently cached ~31-day window and backfills newly published days, but never deletes or touches statistics outside that window.
- Add a manually-configured time-of-use rate schedule (JSON, integration options) and a Calculated TOU Cost sensor per electricity service, since GloBird's API exposes no usable $/kWh rate data (verified against getProductsByAccountId and getAllProductHistoriesByAccountId, which return only plan name/dates, no rates). Calculates cost from real per-interval usage split across your configured Peak/Offpeak/etc. windows.
