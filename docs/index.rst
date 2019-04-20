OpenVAS Reporting
=================

|version| |license| |docs| |vulns| |codecov| |requires| |pypi_version| |pypi_format|

A tool to convert OpenVAS XML into reports.

Table of contents
-----------------

.. toctree::
   :maxdepth: 3

   Welcome <self>
   changelog
   usage/index

What's OpenVAS Reporting?
-------------------------

OpenVAS reporting allows you to create a report from one or more OpenVAS/Greenbone XML reports.
This way, it's easy to create simple graphs for the compliance department, create pivot tables to collect statistics,
or combine multiple scan reports into one.

The tool currently only supports exports to Excel, creating a workbook containing a summary sheet, table of contents
and a worksheet per vulnerability (with info and list of hosts).

.. image:: _static/img/screenshot-report.png
   :alt: Report example screenshot - Summary
   :width: 30%

.. image:: _static/img/screenshot-report1.png
   :alt: Report example screenshot - Table of Contents
   :width: 30%

.. image:: _static/img/screenshot-report2.png
   :alt: Report example screenshot - Vulnerability description
   :width: 30%

Why create this tool?
---------------------

OpenVAS is an awesome tool for many people and it's UI is nice but not always intuitive. It currently also lacks the
ability to merge multiple task reports into one, especially when testing multiple environments. This tool allows you to
merge multiple XML reports into one.

Working with CSV exports of the OpenVAS reports is just a pain, since they include newlines which cause Excel (or other
importers) to view those lines as new inputs. This can be fixed with some find/replace voodoo, which can probably be
automated as well (in tools like Notepad++), but it's just too much hassle to filter out all edge cases.

Or maybe you just prefer working in Excel because you're used to it
(Excel is probably the #1 IT tool across all branches).

Aren't there other tools to achieve this?
-----------------------------------------

As a good netizen, I used some search engine terms to find tools that would fit my needs (merge reports, export to Excel,
perhaps export to other formats) and found cr0hn's `OpenVAS2Report <https://github.com/cr0hn/openvas_to_report>`_.
However, it appears that either the format of the XML reports has changed and the code doesn't handle this well, or my
reports contain some weird voodoo, because some of my reports would convert (partially) while others wouldn't.

It was first thinking of tracking down the error and sending a pull request to fix it. However, at the time I needed a
quick solution and I had no idea where to start tracing the error. So I made a fork of the project, but basically
rewrote chunks of the code (copy/pasting) a lot of it as well.


How can I help?
---------------

I am planning to maintain this tool in the future as to be able to support future changes to the OpenVAS report format.
I also plan on adding more functionality as I feel the need for it, or receive requests from others.

If you feel like I'd need to implement a new feature, rewrite some code, fix a bug, ...
hit me up on `Twitter <https://twitter.com/DezeStijn>`_
or file an issue on `GitHub <https://github.com/TheGroundZero/openvas_to_report>`_.

TODO list
---------

.. todolist::


.. |codecov| image:: https://codecov.io/gh/TheGroundZero/openvasreporting/branch/master/graph/badge.svg
   :alt: Code Coverage
   :target: https://codecov.io/gh/TheGroundZero/openvasreporting
.. |docs| image:: https://readthedocs.org/projects/openvas-reporting/badge/?version=latest&style=flat
   :target: https://openvas-reporting.stijncrevits.be
   :alt: Documentation
.. |license| image:: https://img.shields.io/github/license/TheGroundZero/openvasreporting.svg
   :alt: GitHub
   :target: https://github.com/TheGroundZero/openvasreporting/blob/master/LICENSE
.. |pypi_format| image:: https://img.shields.io/pypi/format/OpenVAS-Reporting.svg
   :alt: PyPI - Format
   :target: https://pypi.org/project/OpenVAS-Reporting/
.. |pypi_version| image:: https://img.shields.io/pypi/v/OpenVAS-Reporting.svg
   :alt: PyPI - Version
   :target: https://pypi.org/project/OpenVAS-Reporting/
.. |requires| image:: https://requires.io/github/TheGroundZero/openvasreporting/requirements.svg?branch=master
   :target: https://requires.io/github/TheGroundZero/openvasreporting/requirements/?branch=master
   :alt: Requirements Status
.. |version| image:: https://badge.fury.io/gh/TheGroundZero%2Fopenvasreporting.svg
   :target: https://badge.fury.io/gh/TheGroundZero%2Fopenvasreporting
.. |vulns| image:: https://snyk.io/test/github/TheGroundZero/openvasreporting/badge.svg?targetFile=requirements.txt
   :alt: Known Vulnerabilities
   :target: https://snyk.io/test/github/TheGroundZero/openvasreporting?targetFile=requirements.txt
