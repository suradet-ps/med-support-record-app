# Medication Support Record System

```
███╗   ███╗███████╗██████╗  ██████╗██╗   ██╗██████╗ ██████╗  ██████╗ ██████╗ ████████╗
████╗ ████║██╔════╝██╔══██╗██╔════╝██║   ██║██╔══██╗██╔══██╗██╔═══██╗██╔══██╗╚══██╔══╝
██╔████╔██║█████╗  ██║  ██║███████╗██║   ██║██████╔╝██████╔╝██║   ██║██████╔╝   ██║
██║╚██╔╝██║██╔══╝  ██║  ██║╚════██║██║   ██║██╔═══╝ ██╔═══╝ ██║   ██║██╔══██╗   ██║
██║ ╚═╝ ██║███████╗██████╔╝██████╔╝╚██████╔╝██║     ██║     ╚██████╔╝██║  ██║   ██║
╚═╝     ╚═╝╚══════╝╚═════╝ ╚═════╝ ╚═════╝ ╚═╝╚═╝ ╚═════╝ ╚═╝  ╚═╝   ╚═╝
```

---

## ◆ PULSE

Support medication values are quick to log and even quicker to lose in a
notebook. This is the record system for the numbers that matter to the
pharmacy budget: a form built for rapid data entry, a Supabase
database that persists the instant the button is pressed, and
feedback that says so - success or failure, announced, never silent.
Mobile-first, pastel-calm, and ready on every screen the pharmacist
carries.

| Form ▣ | Real-time ▣ | Feedback ▣ | Mobile ▣ |
|---|---|---|---|

*The record loop - enter, save, confirm - is sealed.*

> Built with vanilla HTML, CSS, and JavaScript, backed by Supabase,
> shipped from Firebase Hosting - the dependency count is the feature.
>
> **suradet-ps**, artifact keeper

---

## ◆ IGNITION

One clone, zero build step.

```
⟫ git clone https://github.com/suradet-ps/med-support-record-app.git
⟫ cd med-support-record-app
```

Set `SUPABASE_URL` and `SUPABASE_ANON_KEY` in `config.js`, then open
`index.html` in a browser. That is the whole ritual - no bundler, no
install, no server of your own.

<details>
<summary>Environment</summary>

- A [Supabase](https://supabase.io/) project with its API key and
  project URL
- Firebase Hosting for deployment (`firebase.json` included)

</details>

---

## ◆ ANATOMY

One page, one save, an honest confirmation.

- **Enters** - the form is built for rapid entry: the fields a
  pharmacist types during a shift, not a survey.
- **Saves** - every submission reaches Supabase immediately - the
  record exists the moment the button is pressed, not at the end of
  the month.
- **Confirms** - SweetAlert2 announces the outcome: success or
  failure, with the kind of feedback a busy user cannot afford to
  miss.
- **Responds** - Flexbox and media queries carry the form from phone
  to tablet to desktop - the entry point follows the user's screen.
- **Wears** - a pastel yellow redesign keeps the page calm for the
  hours it is used - utility with a quieter face.

---

## ◆ RITUALS

**The core ceremony** - the daily log:

1. Open the page - from the phone, the tablet, or the desktop.
2. Enter the support value; the form accepts it in seconds.
3. Save. Supabase answers instantly; SweetAlert2 confirms.
4. Move on. The record is already in the database, and the month's
   total is one query away.

**The ceremony of the instant save** - the number is persisted when
the button is pressed, not when the shift ends. A forgotten save is a
missing record; the database removes the remembering from the ritual.

**The ceremony of the told result** - every save is announced: success
or failure, never silence. A user who does not know whether the save
landed is a user who will save twice or not at all.

---

## ◆ ECHOES

**Where this artifact is heading**

```
enter    ▸ rapid-entry form interface ──────────────────────────────── ▸ sealed
save     ▸ Supabase instant persistence ────────────────────────────── ▸ sealed
confirm  ▸ SweetAlert2 feedback, success and failure ───────────────── ▸ sealed
respond  ▸ mobile-first layouts across screens ─────────────────────── ▸ sealed
```

**Raising the artifact** - the connection logic lives in `config.js`;
the styles in `style.css`; the behavior in `script.js`. Open an issue
first to discuss a change.

**Status** - dependencies are maintained through Renovate; releases
deploy to Firebase Hosting.

---

```
  ─────────────────────────────────────────
   A value logged late is a value
   half-remembered.
  ─────────────────────────────────────────
```

Licensed under the [MIT License](LICENSE).