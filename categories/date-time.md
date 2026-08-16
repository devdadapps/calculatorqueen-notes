# Date & Time

Date and time articles handle durations, calendar arithmetic, schedules, business days, or time-zone conversions. The central challenge is deciding which clock and calendar rules apply before subtracting numbers.

## Calendar and zone discipline

Inputs distinguish dates, local date-times, UTC instants, elapsed durations, and wall-clock times. The applicable calendar, time zone, daylight-saving rule, inclusive/exclusive endpoint convention, holiday set, and workweek definition are stated. Date-only arithmetic must not silently become a fixed number of seconds.

## Boundaries

Months and years have variable lengths. Daylight-saving transitions can create missing or repeated local times. Historical and future zone rules can change, while business-day results depend on the selected jurisdiction and holiday source. Leap seconds and specialized astronomical time scales require separate treatment.

## Selection standard

Choose questions with a precise timeline model and test cases around month ends, leap years, midnight, and zone transitions. Reject ambiguous prompts until their locale, zone, and endpoint rules are declared.

Published entries will use `YYYY-MM-DD — title — calendar/zone basis — endpoint convention`.

