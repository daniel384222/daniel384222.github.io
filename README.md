# Exam Timer

A single-file, offline exam timer with reading time, working time, pause, and
rule-enforced rest breaks. No install, no internet required after download.

## Use it

Open `exam-timer.html` in any browser (double-click it, or drag it into a
browser window). Everything runs locally — nothing is saved or sent anywhere,
so refreshing the page resets it.

## Set up an exam

1. Enter the course name and exam date.
2. Enter reading time (0 if none) and working time.
3. Enter the rest-break rate from the student's decision letter (minutes per
   half hour — defaults to the standard 5.0).
4. Check the calculated rest-break allowance shown on screen.
5. Click **Set up timer**.

## Run it

- **Start reading time** begins the countdown. It switches to working time on
  its own when reading time runs out.
- **Pause** freezes the clock (use for interruptions); **Resume** continues it.
- **Start rest break** switches to the rest-break clock and pauses working
  time. It's greyed out once less than 5 minutes of allowance remains.
- **End rest break** unlocks after 5 minutes and returns to working time. If
  the allowance runs out mid-break, it ends automatically.
- A running log at the bottom records every break taken, with its length and
  the working time remaining at that point — useful for the supervisor's
  record.
- **Full screen**, **Sound on/off**, and **Reset timer** are at the bottom of
  the page.

## How rest breaks are enforced

- Allowance = rate × complete half hours of **working time only** (reading
  time is never counted).
- No break can be shorter than 5 minutes or push the total over the
  allowance — the buttons simply won't allow it.
- Partial half hours (e.g. the extra 10 minutes in a 2h10m exam) don't add to
  the allowance, matching how the provision is usually applied.

## Files

- `exam-timer.html` — the whole app. Keep it as one file; it has no
  dependencies except a Google Fonts request for Inter (falls back to the
  system font if offline).
