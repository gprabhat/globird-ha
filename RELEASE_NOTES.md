## v0.1.42

- Import half-hourly (or finer, e.g. 5-minute) smart-meter usage into Home Assistant recorder long-term statistics via the Recent Usage Total sensor, so the Energy Dashboard can show real consumption shape through the day instead of only daily totals.
- Fix a bug where interval usage was double- (or multi-) counted on time-of-use accounts: the portal attaches the same full-day interval array to every Peak/Offpeak row for a meter, and the integration was previously summing it once per row instead of once per meter register.
- Expose a recorder-safe recent window of per-day interval breakdowns as a Recent Usage Total attribute for automations/templates.
- Add a Weather Impacted Days sensor and a meter type description (e.g. "Smart") on Meter Info, using portal data that was already being fetched but not surfaced.
- Add a cost breakdown by time-of-use charge type (e.g. Peak/Offpeak) as a Recent Cost Total attribute, for accounts whose plan bills cost per time-of-use period.
