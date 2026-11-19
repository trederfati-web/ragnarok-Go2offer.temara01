# Tracking handoff

The landing page keeps analytics off by default. After the client approves the data flow and consent requirements, set `window.RTNW_ANALYTICS_ENABLED = true` before the inline page script runs and connect `window.dataLayer` to the approved tag manager.

The page defaults to English. It selects Indonesian when any browser language preference is Indonesian (`id` or `id-*`); all other preferences show English. This behavior applies across the target GEOs: Indonesia, Taiwan, the Philippines, and other ASEAN markets. There is no manual language switch. The `angle=explore` and `angle=nostalgia` message tests remain available.

Events prepared by the page:

- `lp_view` — language, GEO, device class, and available UTM fields.
- `steam_outbound_click` — exact Steam destination, CTA placement, and available UTM fields.

These are diagnostic events only. A Steam click is not an install, account creation, or First Login. `steam_install`, `gravity_account_created` / `launcher_auth`, and the conversion event `first_login` need approved integrations and a verified backend definition. Do not report First Login from this page.

Message test variants are available through `?angle=explore` and `?angle=nostalgia`. Assign traffic consistently at campaign level; the default page uses the exploration angle.

Before paid launch, confirm the Indonesian copy with a native speaker, confirm Indonesian regional/server availability and approved game assets with Gravity, review Steam's current PC requirements, and test the First Login attribution path end-to-end.
