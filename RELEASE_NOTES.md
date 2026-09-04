## v0.1.44

- Fix a MALFORMED_ARGUMENT error when opening integration options: the options description text embedded a raw JSON example with curly braces, which Home Assistant's frontend interprets as ICU MessageFormat placeholders. The example was likely breaking the options form before a TOU rate schedule could be saved, leaving the Calculated TOU Cost sensor stuck unavailable even after entering a schedule. Removed the inline JSON from the translated string (kept in the README instead) and synced the previously-stale strings.json with translations/en.json.
