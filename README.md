# transfer-form

Registration form for the Saudi health-sector transfer bot
([طلبات النقل بالبديل](https://t.me/bdeel_moh_bot)), served as a Telegram Mini App.

The page is static and has no backend: on submit it calls
`Telegram.WebApp.sendData()`, and Telegram delivers the JSON to the bot over the
connection it already has. The bot re-validates every field before storing it.

`index.html` is **generated** — edit `webapp/index.template.html` in the bot
project and re-run `build_webapp.py`, which bakes the specialty and area lists
in from the gazetteer so the form cannot drift from the matcher.
