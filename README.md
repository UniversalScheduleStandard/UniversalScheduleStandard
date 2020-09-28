<p align="center">
  <img src="images/uss_logo-01.svg" alt="USS Logo" width="537" height="205">
</p>

<h3 align="center" style="margin-bottom: 16px">Proposal for a standardized format to store and transport <br /><a href="https://en.wikipedia.org/wiki/Shooting_schedule">production schedules</a> and <a href="https://en.wikipedia.org/wiki/Script_breakdown">breakdowns</a> across the entertainment industry.</h3>

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
</p>
<p align="center">:star: Star us on GitHub!</p>
 -->
# The Problem

<img src="images/no_communication.png" alt="No Communication" width="300" height="211" align="right"/>

Production schedules are indispensible documents in the entertainment industry, containing the core information that is consumed both during prep and on set. 

An increasing number of software tools have been created that either create or consume this schedule data. Unfortuately, the creators of these tools and their users are now finding that there is no easy way to transport this data from one application to another. 

When transportability problems like this have occurred in the past, creators have tended to generate their own custom import/export solutions. This inevitably results in a fractured landscape of multiple file formats that need to be maintained and supported.

Additionally, unnecessary resources are placed on promoting file formats, which bring little value to their creators and only serve to ultimately annoy the end user. 

# The Solution - **Universal Schedule Standard**

<img src="images/communication.png" alt="Communication" width="300" height="211" align="right"/>

The **Universal Schedule Standard** is a proposal for one common method to store and transport schedule and breakdown data across all existing and future platforms. 

Using one standard makes the user's data portable allowing them to create a schedule in one application and then transfer that information to another application that might create budgets, call sheets or other useful end products. 

Each company using the standard will reduce their work load, as they can avoid supporting myriad competing formats. These various applications will be lighter and more easily managable with only one import/export format to support. 

And perhaps most importantly, end users will gain confidence in the entire sector and will more freely use multiple services, with the knowledge that their data is always portable and safe. 

# Features

The standard proposed here has been carefully crafted to serve all sectors of the entertainment industry. Easily allowing for:

- Transport - use it to easily move entire schedules or breakdowns between applications or services
- Storage - provides a common format for legacy data
- Future Proofing - stores data in a simple text format that will be easily readable by any system in the future
- Flexibility - the schedule and breakdown data are stored separately, allowing for the storage of just breakdown data without a schedule, if desired
- Storage of Metadata - includes important additional data such as calendars, multiple stripboards, individual settings for elements, etc.
- Conforms to the [Universal Category Identification](https://github.com/thinkcrew/UniversalCategoryIdentification) standard so that all breakdown categories are easily parsed
- Open standard - no licensing fees - free to use
- Not reliant on any third party resources or services
- Is easily extensible if you'd like to store additional data
- Works interchangably as a file and as data in an API call

# Details

This proposed standard has been designed as a conscise way to store as much schedule and breakdown data as possible in a format that is both human and machine readable.

The schedule and breakdown data are stored in JSON format, allowing for easily parsable import/export operations either in a saved file or through an API call. 

Here is an example of the entire standard object:

```json
{
  "universalScheduleStandard": {
    "id": "5d9fc8cfc0efae0017a32a11",
    "author": "Jane Smith",
    "created": "2020-10-07T00:12:06.000Z",
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

The last five items in this object are where the schedule and breakdown data are stored. That data is merely a series of additional sub-objects that are stored in those arrays.

# Examples

See the [sample file](/samples/schedule.uss) in the [/samples](samples/) folder for a full example. To keep the sample file as readable as possible, it only contains one scene and a few elements. A full schedule would of course contain more data.

# Documentation

For detailed instructions about the structure and format of the standard object, please read the [detailed documentation](docs/docs.md) found in the [/docs](docs/) folder. 

# Feeback & Participation in the Proposal 🎉

Any creator can participate in the finalization of this proposed standard. Please post [pull requests](/pulls) or [issues](/issues) with update ideas, discussion or suggestions. 

This proposal is intended to foster the communication of ideas and ultimately result in the completion of a universal standard that can be used by any creator in the industry. 

As these are early days, it is not recommended that you implement this standard yet. After we've gotten some feedback we'll have a better idea of when implementation will be advised. 

<!-- # Collaborators

We are proud to have the following collaborators on this standard:

- Think Crew -->

# License

<a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">
  <img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">Creative Commons Attribution-NoDerivatives 4.0 International License.
</a>
