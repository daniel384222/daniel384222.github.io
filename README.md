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
- **Break length** (on the rest-break screen) is how long the student intends
  this break to last, e.g. `05:00`. The clock counts it down and the break
  ends on its own when it runs out. The student can change it mid-break
  (to extend if they're not rested yet) within the rules: never under 5:00
  and never more than the allowance left.
- **End rest break now** unlocks after 5 minutes for ending a break early.
- A running log at the bottom records every break taken, with its length and
  the working time remaining at that point — useful for the supervisor's
  record.
- **Full screen**, **Sound on/off**, and **Reset timer** are at the bottom of
  the page.

## How rest breaks are enforced

- Allowance = rate × complete half hours of **total exam time** (reading +
  working). E.g. 10 min reading + 2h 20m working = 2h 30m = 5 half hours
  × 5 min = 25 minutes. Breaks themselves can only be taken during working
  time.
- No break can be shorter than 5 minutes or push the total over the
  allowance — the buttons simply won't allow it.
- Partial half hours (e.g. the extra 10 minutes in a 2h10m exam) don't add to
  the allowance, matching how the provision is usually applied.
- If the browser tab is suspended mid-break, any time beyond the planned
  length or the allowance is charged to working time, never gained.

## Files

- `exam-timer.html` — the whole app. Keep it as one file; it has no
  dependencies except a Google Fonts request for Inter (falls back to the
  system font if offline).
