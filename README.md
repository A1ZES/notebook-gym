# NoteBook Gym

A quick gym notebook.

- **Today**: pick one of your workouts, tap the exercise, set kg and reps, tap **Log set**.
  Make workouts with **+ New** (a name and the list of exercises, in order); change them with **Edit workout**.
- **Notes**: a page of notes for each day. It saves as you type.
- **Weight**: log your body weight once a day and see the trend.
- **History**: past days as notebook pages, with that day's note.

Data is stored in Supabase, one row per user per item, protected by row-level security:
`sets` (machine, kg, reps, logged_at), `workouts` (name, machines[]), `notes` (day, body), `weights` (day, kg).
Everything is saved on the device first and sent to Supabase when there is signal.

Open the site on iPhone in Safari → Share → Add to Home Screen.
