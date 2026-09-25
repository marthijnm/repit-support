# Repit User Manual

Repit is a focused strength-training log. Use it to plan workouts, track sets,
review your history, and follow your progress.

## Getting started

1. Open **Today**.
2. Start a workout from a template, or choose an empty workout.
3. Enter the reps and weight for each set and mark completed sets with the
   completion control.
4. Add, replace, reorder, or remove exercises when needed.
5. Tap **Finish** when the workout is complete.

Repit allows one workout per calendar day and one active workout at a time. An
unfinished workout from an earlier day must be finished or cancelled before a
new workout can be started.

## Exercises

The **Exercises** tab contains the exercise library. You can search by exercise
name or muscle group and sort the list by name, usage, or most recent use.

Each exercise has one primary muscle group, optional secondary muscle groups,
and optional notes. Custom exercises can be created and existing exercises can
be edited.

An exercise cannot be deleted while it is used by a template, an active
workout, or workout history. This protects existing training data.

Open an exercise to see its personal records and links to its history and
progress chart.

## Workout templates

The **Templates** tab contains reusable workout plans. A template defines:

- The exercises and their order.
- The number of sets for each exercise.
- Starting values for reps and weight.

Templates can be created, edited, duplicated, and deleted. You can also create
a new exercise while editing a template.

When a workout is started, the template determines its structure. Repit uses
the most recent relevant completed sets to suggest reps and weight, preferring
history from the same template. Template values are used when no suitable
history exists.

Deleting a template does not delete completed workouts that used it.

## Active workouts

Start a template workout or an empty workout from **Today**. An empty workout
starts without exercises; at least one exercise and one set per exercise are
required before it can be finished.

During a workout you can:

- Add, replace, reorder, or remove exercises.
- Add or remove sets.
- Change reps and weight.
- Mark sets as completed or reopen them.
- Open exercise history and progress.
- Show or hide exercise notes.

An exercise with completed sets cannot be replaced or removed. The same
exercise cannot appear twice in one workout.

If **Hide completed exercises** is enabled, an exercise is hidden when all its
sets are complete. The setting is remembered for future workouts.

If an active workout was started on an earlier day, Repit shows a prominent
notice with actions to continue, complete, or cancel it. Completing follows the
normal unfinished-set and self-assessment flow; cancelling still requires
confirmation.

### Rest timer

Open the rest timer from the workout toolbar. Choose a preset duration or a
custom duration from 5 seconds to 10 minutes.

While the timer is running, you can add or remove 10 seconds or skip the timer.
With notification permission, Repit sends a local notification when the timer
ends. The timer remains linked to the active workout when the app moves to the
background or restarts. Finishing or cancelling that workout also clears its
timer.

### Finishing or cancelling

If unfinished sets remain when you finish, Repit asks you to:

- Mark the unfinished sets as completed.
- Remove the unfinished sets and exercises without completed sets.
- Continue the workout.

Repit never silently completes unfinished sets.

Cancelling permanently removes the active workout and its entered data.

## Self-assessment

Enable **Self-assessment** in Settings to record how a workout felt. A
self-assessment contains:

- Perceived condition from **Very weak** to **Very strong**.
- Perceived exertion from 0 to 10.
- An optional note.

The assessment is optional even when the feature is enabled. Turning the
setting off does not delete or hide assessments already stored with completed
workouts.

## History and completed workouts

The **History** tab shows completed workouts in a monthly calendar and list.
Open a workout to review its times, exercises, sets, estimated one-rep max, and
optional self-assessment.

For an existing completed workout, you can correct the reps and weight of its
sets. Other workout details and structure cannot currently be edited.

Use **Save as template** to create an editable template draft from a completed
workout. Saving the template does not change the historical workout or its
original template.

Completed workouts can also be deleted. Deleting one makes that calendar day
available again.

### Adding a completed workout manually

From History, add a completed workout for today or an earlier date. Select its
date, start and end times, and a template, then adjust its exercises and sets as
needed. The end time must be after the start time and cannot be in the future.
The selected calendar day must not already contain a workout.

## Progress and Insights

Repit calculates performance only from completed workouts and completed sets.

Exercise details include these personal records:

- **Estimated 1RM:** the highest estimated one-rep max.
- **Best set:** the heaviest completed set, with reps used as a tie-breaker.
- **Best volume:** the highest total completed-set volume in one workout.

Estimated 1RM is an estimate, not a measured maximum. For sets above one rep,
Repit uses `weight × (1 + reps / 30)` and keeps the highest result for the
exercise in that workout.

Exercise progress charts show current, best, and trend values over a selected
date range.

Open **Insights** from History to review:

- Training consistency and workouts per week.
- Completed sets per week, optionally filtered by primary muscle group.
- Condition history.
- Perceived exertion history.

Weeks follow the device's calendar and regional settings. Higher exertion is
not treated as inherently good or bad; it describes how demanding a workout
felt.

## Settings

### Weight units

Choose **Metric (kg)** or **Imperial (lbs)**. This changes input, display, and
chart units. Stored weights are not changed when you switch units.

### Active workout reminders

**Remind me about an active workout** is enabled by default. With notification
permission, Repit sends one reminder after two hours without changes to the
active workout. Activity before that deadline moves the reminder to two hours
after the latest change.

Only one reminder is sent per workout. Finishing or cancelling the workout, or
turning the setting off, clears its reminder. Notification permission is
optional and does not affect workout logging.

### Exporting a backup

Export creates a JSON backup containing exercises, templates, completed
workouts, settings, and app-version information. The workout-reminder preference
is part of the settings. Active workouts, active rest timers, and pending workout
reminders are not included.

Keep exported files in a safe location if you want an independent copy of your
training data.

### Importing a backup

Select a Repit JSON backup and review the preview before importing. Import uses
record identity, not names:

- A record with the same identity is replaced by the imported record.
- A new record is added.
- A local record missing from the backup is kept.

Replacing a template or workout also replaces its contained exercises and sets;
they are not merged individually. Enable **Import settings** only if the backup's
settings should replace the current settings.

Repit validates the complete result and creates a recovery copy before applying
an import. If validation or saving fails, the current data remains unchanged.

### Recovery copies

Repit creates internal recovery copies before imports and restores. You can
preview available copies in Settings.

Restoring a recovery copy replaces all current Repit data; it does not merge
records. Repit first creates another recovery copy of the current data so that
the restore can be reversed if necessary.

## Important limits

- One workout is allowed per calendar day.
- Only one workout can be active at a time.
- An exercise can appear only once in a template or workout.
- A completed workout needs at least one exercise and one set per exercise.
- A set supports 1 to 999 reps and a non-negative weight up to 1,000 kg.
- An exercise entry supports up to 100 sets.
- Repit does not currently provide accounts, cloud sync, or active-workout
  export and import.

## Support

For questions, feedback, or problems, open **About Repit** from Today or
Settings and choose **Email Support**.
