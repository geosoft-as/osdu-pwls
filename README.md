# OSDU Practical Well Log Standard (PWLS)

The [OSDU](https://osduforum.org/OSDU) _Practical Well Log Standard_ (PWLS) provides an industry-agreed list of logging tool
classes and a hierarchy of measurement properties and applies all known log mnemonics to them.
When this information is implemented in stores or software, it supports queries over large
populations of log data, making it easier for oil and gas professionals to find and use this
valuable data.

PWLS exists in the following versions:

* [v3.0](https://energistics.org/practical-well-log-standard) (February 25, 2021)
* [v2.0](https://energistics.org/sites/default/files/2023-03/pwls_20.htm) (September 30, 2003)
* [v1.0](https://energistics.org/sites/default/files/2023-03/pwls_10.htm) (February 27, 2001)

They are defined by static MS/Excel spreadsheets which represents a problem: The PWLS
contains _dynamic_ content and in order to be useful there must be a way to keep the
standard continuously updated as well as propagating such updates to software and other entities
that depend on the standard.


## The GeoSoft approach

GeoSoft has addressed the static nature of PWLS by redefining it in the
[JSON](https://en.wikipedia.org/wiki/JSON)
format and publishing it on
[GitHub](https://github.com/geosoft-as/pwls)
and thereby utilizing the
[Git](https://en.wikipedia.org/wiki/Git)
distributed versioning control system.

The idea is that PWSL _contributors_ (service companies typically)
can update the standard through Git
[_pull requests_](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
and get these reviewed and accepted by OSDU/GeoSoft moderators.
Software that is using PWLS will then instantly update whenever the standard changes.

Using Git as the versioning control system ensures proper version control and traceability
of changes and makes _explicit_ versioning of the standard redundant.


## Repository content

The present repository contains the following:

* `excel/*` The original PWLS v3.0 MS/Excel spreadsheet included for reference
* `json/*`  The dynamic JSON definition of PWSL


## How to contribute

In order to provide updates to the PWLS standard
make sure you have a valid GitHub user account, else sign up [here](https://github.com/).
When this is in place, please submit standard pull requests to the repository.
For completeness, a quick guideline is provided below:

1. Go to [pwls](https://github.com/geosoft-as/pwls) and click _Fork_ to create a copy of the repository in your account
1. Clone the fork to your local machine by `git clone https://github.com/<username>/pwls.git`
1. Navigate to the repository's directory: `cd pwls`
1. Create a new branch for the updates: `git checkout -b <branch-name>`
1. Make the required changes to the PWLS JSON files
1. Commit the changes: `git commit -am "Description of changes"`
1. Push changes to your fork: `git push origin <branch-name>`
1. Go to [pwls](https://github.com/geosoft-as/pwls) and click _New pull request_
1. Select the branch (&lt;branch-name&gt;) you pushed your changes to
1. Submit the pull request with a description of your changes

The changes will then be reviewed/accepted or commented/rejected by the
repository moderators.


## Associated technologies

The related [jpwls](https://github.com/geosoft-as/jpwls) repository contains a Java
implementation of the PWLS standard. It can be used in two different ways:

* As a REST API web service where clients can request updated PWLS information at any time
* As a library (jpwls.jar) that can be embedded in any Java application

A REST API _Proof of Concept_ (PoC) implementation hosted in Amazon Web Services (AWS) is
available [here](http://13.60.27.155).
This API can be utilized by any technology that can digest JSON formatted
information. See [jpwls](https://github.com/geosoft-as/jpwls) for details.


## Contact

For inquiries on the GeoSoft PWLS implementation please contact
[info@geosoft.no](mailto:info@geosoft.no)
