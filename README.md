# NoteBook Gym

A quick gym notebook. Private beta: only the owner's account can log in.

The home screen shows everything at once: four tiles and the last 7 days. Each tile opens its own screen; **‹ Home** (or the phone's back gesture) returns.

- **Train**: pick one of your workouts, or **Free** to choose from every exercise (or type a new one). Tap the exercise, set kg and reps, tap **Log set**.
  Make workouts with **+ New workout** (a name and the list of exercises, in order); change them with **Edit workout**.
- **Weight**: log your body weight once a day and see the trend.
- **Notes**: a page of notes for each day. It saves as you type.
- **History**: past days as notebook pages, with that day's note.

Data is stored in Supabase, one row per user per item, protected by row-level security:
`sets` (machine, kg, reps, logged_at), `workouts` (name, machines[]), `notes` (day, body), `weights` (day, kg).
Everything is saved on the device first and sent to Supabase when there is signal.

Open the site on iPhone in Safari → Share → Add to Home Screen.
