---
layout: default
title: NSISO8601DateFormatter / ISO8601DateFormatter
categories: [Foundation]
---

<https://developer.apple.com/documentation/foundation/iso8601dateformatter>

Date format specifiers referenced in Apple's documentation and on this page are defined at <https://www.unicode.org/reports/tr35/tr35-31/tr35-dates.html#Date_Format_Patterns>.

### [ISO8601DateFormatter.Options](https://developer.apple.com/documentation/foundation/iso8601dateformatter/options)

`withYear`, `withMonth`, `withDay`, `withTime`, and `withTimeZone` produce no output if specified individually with no other options. If paired with any other option, even one that should not change the output (e.g. `[.withYear, .withColonSeparatorInTime]`), they behave as expected. ([7424712](https://feedbackassistant.apple.com/feedback/7424712))

`.withFullDate` also includes `.withDashSeparatorInDate`. ([7424712](https://feedbackassistant.apple.com/feedback/7424712))

`.withTimeZone` uses the format specifier "ZZZZZ" when the timezone is GMT/UTC, otherwise it uses "Z". ([7424712](https://feedbackassistant.apple.com/feedback/7424712))

`.withTime` as implemented uses `HHmmss` not `HH:mm:ss`. ([7424674](https://feedbackassistant.apple.com/feedback/7424674))

`.withFullTime` as implemented is equivalent to `[.withTime, .withColonSeparatorInTime, .withTimezone, .withColonSeparatorInTimeZone]`. ([7424674](https://feedbackassistant.apple.com/feedback/7424674))

`.withTimeZone` is documented to use the format specifier "ZZZZZ", but what would make withColonSeparatorInTimeZone redundant, so it appears the actual specifier used is "Z". ([7424674](https://feedbackassistant.apple.com/feedback/7424674))
