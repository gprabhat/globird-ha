## v0.1.48

- Add an Account Cost Summary sensor using GloBird's own `/api/transaction/getaccountcostsummary` endpoint, which returns the portal's own running cost estimate (`totalCost`/`totalFeedInCost`) over a date range the portal itself chooses, typically since the account's last switch or cost reset. Distinct from the locally-projected Expected Monthly Cost/Billing Period Cost sensors, which use a different method and date range.
