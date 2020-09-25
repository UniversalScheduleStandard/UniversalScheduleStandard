# entertainmentIndustryScheduleFormat
A proposal for a standardized format for exporting [schedules](https://en.wikipedia.org/wiki/Shooting_schedule) or [script breakdowns](https://en.wikipedia.org/wiki/Script_breakdown) in the entertainment industry.

Two standards are necessary to facilitate this goal:

1) Standard for naming and identifying category types
2) Standard format for exporting the breakdown of a script that includes categories, elements and breakdown sheets

Breakdowns contain data objects of three types: 'scene', 'day' and 'banner'. The inclusion of the last two types would only be used when exporting a schedule. Without days and banners, the export would just be considered a breakdown. When exporting schedules the array of breakdowns would be ordered to match the order of the scenes in the schedule.

See the files in the [/samples](https://github.com/thinkcrew/entertainmentIndustryScheduleFormat/tree/master/samples) folder for examples.
