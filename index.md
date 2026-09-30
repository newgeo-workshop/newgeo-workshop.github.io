---
layout: default
---

{% comment %}
==============================================================================
All page content lives in this file, as plain Markdown.

  * The {#id} after each ## heading is what the nav links point at.
    Keep them if you rename a heading.
  * site.workshop_date pulls the date from _config.yml — edit it there and
    every mention on the page updates.
  * Blockquotes (> ...) render as grey italic notices.

These {% raw %}{% comment %}{% endraw %} blocks are stripped at build time and
never appear in the published page.
==============================================================================
{% endcomment %}

## Overview {#overview}

IP geolocation — the practice of mapping virtual IP addresses to physical locations —
underpins a wide range of Internet services and operations, from content delivery and
targeted advertising to regulatory compliance, fraud detection, policy enforcement, and law
enforcement. Despite its pervasive use, the reliability, accuracy, and transparency of IP
geolocation techniques, databases, and policies remain only partially understood. The
December 2025 [IAB Workshop on IP Address
Geolocation](https://datatracker.ietf.org/group/ipgeows/about/) surfaced fundamental open
questions about accuracy and integrity, the limitations of self-publishing mechanisms such as
geofeeds (RFC 8805), and architectural tensions between passive location inference and
evolving privacy expectations, and its report explicitly recommends further research. At the
same time, IPv6 adoption, VPNs and relay services, CGNAT, satellite-based access, and
regulatory frameworks such as the EU's GDPR and Digital Services Act all challenge current
geolocation assumptions.

Yet there is no dedicated academic venue for measurement work on IP geolocation. Relevant
papers appear sporadically across IMC, CoNEXT, PAM, TMA, SIGCOMM, and security conferences,
but the community lacks a focused forum to consolidate findings, compare methodologies,
benchmark datasets, and build shared infrastructure. NewGeo fills this gap by bringing
together researchers, network operators, geolocation data providers, and policymakers in a
structured workshop co-located with IMC.

## News {#news}

{% comment %} Add new items at the top of this list. {% endcomment %}

- **2026-09-30**: Published the [workshop program](#program) and [venue room](#venue).
- **2026-09-22**: Posted camera-ready instructions.
- **2026-08-20**: Added HotCRP submission site.
- **2026-08-07**: Workshop website launched.
- **2026-07-07**: NewGeo was accepted as an ACM IMC 2026 workshop.

## Call for Papers {#cfp}

IP geolocation is a foundational building block for Internet services, network operations,
and regulatory compliance. Yet the mechanisms underpinning it — commercial geolocation
databases, geofeeds, active probing, and latency-based inference — are insufficiently
understood, inconsistently accurate, and increasingly challenged by architectural shifts in
the Internet. NewGeo 2026 invites original research contributions that advance our
understanding of IP geolocation through rigorous measurement and analysis.

### Topics of Interest

We solicit short papers on topics including, but not limited to:

- Measurement and analysis of geofeeds and other IP geolocation databases
- Novel active and passive geolocation techniques that accommodate emerging Internet
  architectures (VPNs, relays, cellular and mobile, IPv6, CGNAT, address sharing, etc.)
- Geolocation challenges for satellite-based and deep space Internet access
- Ground truth collection methodologies and benchmark datasets
- Artificial Intelligence-based approaches for IP geolocation, validation, or verification
- Longitudinal studies of geolocation accuracy and database evolution
- Applications and implications of IP geolocation for content delivery, regulatory
  compliance, fraud detection, and censorship measurement
- Privacy implications of IP geolocation and location inference
- Reproducibility studies of previously published geolocation measurement work

### Submission Guidelines

Submissions must be original work not previously published and not under review elsewhere.
Papers must be at most **4 pages in length, excluding references** with an optional one page appendix.
Papers are to be formatted according to the ACM two-column `sigconf` style using the [ACM template](https://www.acm.org/publications/proceedings-template) in letterpaper format with a font size of 10pt.
You can use the following LaTeX documentclass:

```latex
\documentclass[10pt,sigconf,letterpaper,anonymous,nonacm]{acmart}
```

All submissions will undergo **double-blind** peer review by the program committee, i.e., submissions must be anonymised: omit author names and affiliations, and refer to your own prior work in the third person.
Papers violating the submission guidelines will be desk-rejected.
Accepted papers will be presented at the workshop, and at least one author of each paper is expected to attend in-person.

Authors must adhere to the [ACM's author guidelines on the use of Generative AI](https://www.acm.org/publications/policies/frequently-asked-questions).
See the [IMC 2026 submission instructions](https://conferences.sigcomm.org/imc/2026/submission-instructions/) for general formatting guidance.

Authors are encouraged to make their measurement data and analysis code available to support
reproducibility.

### Submission Site

{% comment %} Replace this paragraph with the HotCRP link once it is available. {% endcomment %}

Submissions via HotCRP: [https://newgeo26.hotcrp.com/](https://newgeo26.hotcrp.com/). 

### Camera-ready Instructions

Authors of accepted papers should prepare their camera-ready version using the following LaTeX documentclass:

```latex
\documentclass[9pt,sigconf,letterpaper,nonacm]{acmart}
```

To show the workshop name, date, and venue in the page header, add the following to your preamble.
This is needed because the `nonacm` option otherwise removes the conference information from the header.

```latex
\acmConference[NewGeo '26]{New Directions in IP Geolocation Workshop}{October 12, 2026}{Karlsruhe, Germany}
\makeatletter
\AtBeginDocument{\fancyhead[LE,RO]{\@headfootfont\acmConference@shortname,
  \acmConference@date, \acmConference@venue}}
\makeatother
```

Please de-anonymize your paper: remove the `anonymous` option, add all author names and affiliations, and restore any content that was anonymized for review (e.g., self-citations, acknowledgments, project names, and links to code or data).
Please also address the reviewers' comments.

Upload the final version of your paper as a PDF to [HotCRP](https://newgeo26.hotcrp.com/) by **{{ site.camera_ready_date }}**.
Accepted papers will be made available on the workshop website.

## Important Dates {#dates}

> All deadlines are 23:59 AoE (UTC−12).

{% comment %} All four dates are set in _config.yml. {% endcomment %}

| Milestone | Date |
| --- | --- |
| Paper submission deadline | {{ site.submission_date }} |
| Notification of acceptance | {{ site.notification_date }} |
| Camera-ready deadline | {{ site.camera_ready_date }} |
| Workshop | {{ site.workshop_date }} |

## Program {#program}

{% comment %}
Keep `{: .program}` on the line directly beneath the table — that marker is what
stops the time ranges from wrapping mid-range. Within a cell, <br> starts a new
line (one per paper).
{% endcomment %}

| Time | Activity |
| --- | --- |
| 09:00–09:20 | **Welcome by the Chairs**<br>Oliver Gasser & Robert Beverly<br>*Open challenges in IP geolocation, why we started NewGeo, and plans for a workshop report in ACM SIGCOMM CCR — collaborators welcome* |
| 09:20–10:40 | **Session 1: A Fresh Look at Geolocation**<br>Diagnosing Accuracy Limitations in Constraint-Based IP Geolocation<br>Through the Looking Glass: Analyzing Geolocation Providers using Looking Glasses and Active Measurements<br>Reactive Constraint-Based Geolocation of Internet Hosts<br>RIPE Atlas Measurements and Geolocation Providers: A Longitudinal Consistency Evaluation |
| 10:40–11:00 | **Break** with refreshments |
| 11:00–12:00 | **Session 2: Novel Technologies**<br>Where Does This IP Think It Is? Geolocation Accuracy in the Age of Starlink, CGNAT, and Geofeeds<br>A First Look at Starlink's Geofeeds: On Discrepancies between Feeds and Routing<br>Leveraging Large Language Models to Locate Routers: Using LLMs for Parsing rDNS Hostnames |
| 12:00–12:10 | **Closing Remarks**<br>Robert Beverly & Oliver Gasser |
{: .program}

## Committee {#committee}

### Workshop Chairs

| Chair | Affiliation | Contact |
| --- | --- | --- |
| Oliver Gasser | IPinfo | <oliver@ipinfo.io> |
| Robert Beverly | San Diego State University | <rbeverly@sdsu.edu> |

### Program Committee

{% comment %}
Add new members as rows in the table below. Please list name and affiliation
only — do not publish PC members' email addresses.
{% endcomment %}

| Member | Affiliation |
| --- | --- |
| Francesco Bronzino | ENS Lyon |
| Ioana Livadariu | Simula |
| Johanna Ullrich | IT-U Linz |
| Kevin Vermeulen | Ecole Polytechnique |
| Mirja Kühlewind | Ericsson |
| Patrick Sattler | BENOCS |
| Phillipa Gill | Google |
| Sangeetha Abdu Jyothi | UC Irvine |
| Stephen Strowes | Fastly |
| Thomas Krenc | IIJ |
| Vasilis Giotsas | Cloudflare |

## Venue & Attendance {#venue}

NewGeo 2026 takes place on **{{ site.workshop_date }}**, co-located with [ACM IMC 2026](https://conferences.sigcomm.org/imc/2026/) in Karlsruhe, Germany. The workshop is held in the [Engler-Bunte-Hörsaal (40.50)](https://www.kit.edu/campusplan/?id=40.50) at KIT.

Attendance is handled through the standard [IMC 2026 registration](https://conferences.sigcomm.org/imc/2026/registration/) process.
NewGeo is also listed among the [IMC 2026 co-located events](https://conferences.sigcomm.org/imc/2026/events/newgeo/).

The workshop welcomes participation from academic researchers, network operators, geolocation data providers, RIR staff, Internet standardization contributors, and policymakers.

## Contact {#contact}

For questions about the workshop, please contact the chairs:
[Oliver Gasser](mailto:oliver@ipinfo.io) and [Robert Beverly](mailto:rbeverly@sdsu.edu).
