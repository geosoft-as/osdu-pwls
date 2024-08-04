# OSDU Practical Well Log Standard (PWLS)

The Practical Well Log Standard (PWLS) provides an industry-agreed list of logging tool
classes and a hierarchy of measurement properties and applies all known log mnemonics to them.
When this information is implemented in stores or software, it supports queries over large
populations of log data, making it easier for oil and gas professionals to find and use this
valuable data.

PWLS exists in two versions:

* v1.0 released @ September 1, 2001
* v3.0 released @ February 25, 2021

Both are defined by static MS/Excel spreadsheets which represents a problem: The PWLS
contains _dynamic_ content and in order to be useful there must be a way to keep the
standard continously updated as well as propagating such updates to software that utilize
this information.


# GeoSoft PWLS

GeoSoft has adressed the static nature of PWLS by redefining it in the JSON format and
publishing it on GitHub. The idea is that PWSL _contributors_ (service companies typically)
can update the standard through Git _pull requests_ and get these accepted and implemented
by OSDU moderators. Software that utilize PWLS will then be instantly updated whenever
the standard changes.

Using Git as back-end management system ensures proper version control and traceability
of all changes made to the standard, and makes explicit versioning of the standard redundant.


# Repository content

The repository content:

* excel/* The original PWLS v3.0 MS/Excel spreadsheet for reference
* json/*  The JSON equivalent


