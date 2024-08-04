# OSDU Practical Well Log Standard (PWLS)

The Practical Well Log Standard (PWLS) provides an industry-agreed list of logging tool
classes and a hierarchy of measurement properties and applies all known log mnemonics to them.
When this information is implemented in stores or software, it supports queries over large
populations of log data, making it easier for oil and gas professionals to find and use this
valuable data.

PWLS exists in the following versions:

* [v1.0](https://energistics.org/sites/default/files/2023-03/pwls_10.htm) @ February 27, 2001
* [v2.0](https://energistics.org/sites/default/files/2023-03/pwls_20.htm) @ September 30, 2003
* [v3.0](https://energistics.org/practical-well-log-standard) @ February 25, 2021

Both are defined by static MS/Excel spreadsheets which represents a problem: The PWLS
contains _dynamic_ content and in order to be useful there must be a way to keep the
standard continously updated as well as propagating such updates to software and other entities
that depend on the standard.


# GeoSoft PWLS

GeoSoft has adressed the static nature of PWLS by redefining it in the
[JSON](https://en.wikipedia.org/wiki/JSON)
format and publishing it on
[GitHub](https://github.com/geosoft-as/pwls] and thereby utilizing the
[Git](https://en.wikipedia.org/wiki/Git) distributed versioning control system.

The idea is that PWSL _contributors_ (service companies typically)
can update the standard through
Git [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests](_pull requests_)
and get these accepted by OSDU moderators.
Software that is using PWLS will then be instantly updated whenever
the standard changes.

Using Git as our versioning control system ensures proper version control and traceability
of all changes, and makes explicit versioning of the standard redundant.


# Repository content

The present repository contains the following:

* `excel/*` The original PWLS v3.0 MS/Excel spreadsheet included for reference
* `json/*`  The dynamic JSON definition of PWSL


