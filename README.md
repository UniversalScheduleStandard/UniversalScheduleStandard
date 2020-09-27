<p align="center">
  <img src="images/uss_logo-01.svg" alt="USS Logo" width="537" height="205">
</p>

<h3 align="center" style="margin-bottom: 16px">A proposal for a standardized format to store and transport <br /><a href="https://en.wikipedia.org/wiki/Script_breakdown">script breakdowns</a> and <a href="https://en.wikipedia.org/wiki/Shooting_schedule">production schedules</a> across the entertainment industry.</h3>

---

<!-- <p align="center" style="margin-top: 16px">
  <a href="https://github.com/ArmynC/ArminC-AutoExec/commits/master">
  <img src="https://img.shields.io/github/last-commit/ArmynC/ArminC-AutoExec.svg?style=flat-square&logo=github&logoColor=white"
        alt="GitHub last commit">
  <a href="https://github.com/ArmynC/ArminC-AutoExec/issues">
  <img src="https://img.shields.io/github/issues-raw/ArmynC/ArminC-AutoExec.svg?style=flat-square&logo=github&logoColor=white"
        alt="GitHub issues">
  <a href="https://github.com/ArmynC/ArminC-AutoExec/pulls">
  <img src="https://img.shields.io/github/issues-pr-raw/ArmynC/ArminC-AutoExec.svg?style=flat-square&logo=github&logoColor=white"
        alt="GitHub pull requests">
</p> -->
<p align="center">:star: Star us on GitHub!</p>

# The Problem

<img src="images/no_communication.png" alt="No Communication" width="300" height="211" style="float: right"/>

Production schedules are indispensible documents in the entertainment industry, containing the majority of the information that is consumed in prep and on sets. 

An increasing number of software tools have been created that either create or consume this schedule data. Unfortuately, the creators of these tools and their users are now finding that there is no easy way to transport this data from one application to another. 

When these types of transportability problems have occurred in the past, creators have tended to generate their own custom import/export solutions. This inevitably results in multiple file formats that need to be maintained and supported across all of the creators in a field.

# The Solution - **Universal Schedule Standard**

<img src="images/communication.png" alt="No Communication" width="300" height="211" style="float: right"/>

The **Universal Schedule Standard** is a proposal for one common method to store and transport schedule and breakdown data across all existing and future platforms. 

Using one standard makes the user's data portable allowing them to create a schedule in one application and then transfer that information to another application that might create budgets, call sheets or other useful end products. 

Each company using the standard will reduce their work load, as they will not need to necessarily support myriad competing formats. These various applications will be lighter and more easily managable with only one import/export format to support. 

# Features

The standard proposed here has been carefully crafted to serve all sectors of the entertainment industry. Easily allowing for:

- Use as a transport between applications or services
- Common format for storage of legacy data
- Works both as a file and as data in an API call
- Stores all schedule and breakdown data including multiple stripboards, calendars, individual settings for each element
- Conforms to the [Universal Category Identification](https://github.com/thinkcrew/UniversalCategoryIdentification) standard so that all breakdown categories are easily parsed
- Open standard - no licensing fees
- Not reliant on any third party resources or services

# Details

This standard has been designed as a conscise way to store as much data schedule and breakdown data as possible in a format that is both human and machine readable.

The schedule and breakdown data are stored in JSON format, allowing for human readable and easily parsable input and export operations.

Here is an example of the entire standard object:

```json
{
  "universalScheduleStandard": {
    "id": "5d9fc8cfc0efae0017a32a11",
    "author": "Jane Smith",
    "created": "2020-10-11T00:12:06.000Z",
    "description": "This is a description of the schedule",
    "name": "My schedule name",
    "project": "It's A Wonderful Life",
    "schedColor": "Blue",
    "schedDate": "2020-10-07T07:00:00.000Z",
    "scriptColor": "Yellow",
    "scriptDate": "2020-10-01T07:00:00.000Z",
    "source": "Name of originating site",
    "version": "0.1.0",
    "breakdowns": [],
    "calendars": [],
    "categories": [],
    "elements": [],
    "stripboards": []
    }
  }
}
```

The last five items in this object are where the data is stored. That data is merely a series of additional objects that are stored in arrays.

# Examples

See the files in the [/samples](samples/) folder for a full example.

# Documentation

For more detailed information about the structure and format of the object, please read the [detailed documentation](docs/docs.md) found in the [/docs](docs/) folder. 

# License

<a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">
  <img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">Creative Commons Attribution-NoDerivatives 4.0 International License.
</a>

<!-- # Collaborators

We are proud to have the following collaborators on this standard:

- Think Crew -->

