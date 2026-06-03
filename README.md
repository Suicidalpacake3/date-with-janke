# Will you go on a date with me, Janke? 🤍

A small romantic web app: Janke is asked out (the "No" button politely runs away),
she picks a day, time and date idea, gets a confirmation screen, **you get an email**,
and she can add the date straight to her calendar.

Everything is a single static `index.html` — perfect for **GitHub Pages**.

---

## What it does

1. **Page 1** – "Will you go on a date with me, Janke?" with a *Yes* and a *No* button.
   The *No* button slides away from the cursor and can never be clicked; it glides
   back to its spot when the mouse leaves, then dodges again. Works on touch too.
2. **Page 2** – a date + time picker, a dropdown of date ideas, optional extras
   (flowers, dessert, etc.), and a note field.
3. **Page 3** – "Our date is confirmed 🎉", a summary, **an email sent to you**,
   and **Add to Google Calendar** + **download .ics** buttons.

Your Formspree endpoint (`mykagdba`) and email are already wired in.

---

## Publish it on GitHub Pages (5 minutes)

1. Go to <https://github.com/new> and create a repository, e.g. **`date-with-janke`**
   (Public is fine — Pages needs Public on free accounts).
2. On the new repo page click **uploading an existing file**.
3. Drag in **`index.html`** and **`.nojekyll`** (and this README if you like), then
   **Commit changes**.
4. In the repo go to **Settings → Pages**.
5. Under **Build and deployment → Source** choose **Deploy from a branch**.
6. Set branch to **`main`** and folder to **`/ (root)`**, then **Save**.
7. Wait ~1 minute. Your link appears at the top of that Pages screen:

   ```
   https://YOUR-USERNAME.github.io/date-with-janke/
   ```

Send Janke that link. 🎉

> **Tip:** the `.nojekyll` file is just there to make sure GitHub serves the page
> exactly as-is. If you don't see it after unzipping, you can ignore it — the site
> still works without it.

---

## Where the email goes

When Janke hits **Confirm our date**, the choice is POSTed to your Formspree form
(`https://formspree.io/f/mykagdba`) and Formspree emails **nathanconradienc@gmail.com**
with the day, time, date type, extras and her note.

**First-time only:** Formspree may send *you* a one-time confirmation email the very
first time the form is submitted — click the link in it to activate the form. After
that, every submission lands in your inbox automatically. (Easiest way to activate:
open your own published site once and submit a test.)

---

## Calendar

The confirmation screen gives Janke two options:

- **Add to Google Calendar** – opens a pre-filled Google Calendar event.
- **Download .ics** – a standard calendar file that opens in Apple Calendar,
  Outlook, or Google Calendar.

The same email gives you all the details to add it on your side too. The event is
set to a 2-hour block starting at the chosen time.

---

## Want to tweak something later?

- **Date ideas:** edit the `<select id="dateType">` list in `index.html`.
- **Extras:** edit the checkboxes under "Any little extras?".
- **Wording / colours:** the palette lives in the `:root { ... }` block at the top
  of the file; the headline text is in the Page 1 section.
