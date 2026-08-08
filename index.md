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

Submissions will be handled via HotCRP. The submission URL will be announced here.

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
When the schedule is confirmed, replace the line below with a Markdown table and
keep `{: .program}` on the line directly beneath it — that marker is what stops
the time ranges from wrapping mid-range:

| Time | Activity |
| --- | --- |
| 09:00–09:10 | **Opening remarks** |
{: .program}
{% endcomment %}

TBD — the workshop program will be announced here once the accepted papers and scheduling
are confirmed.

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
| Mirja Kühlewind | Ericsson |
| Patrick Sattler | BENOCS |
| Phillipa Gill | Google |
| Sangeetha Abdu Jyothi | UC Irvine |
| Stephen Strowes | Fastly |
| Thomas Krenc | IIJ |
| Vasilis Giotsas | Cloudflare |

## Venue & Attendance {#venue}

NewGeo 2026 takes place on **{{ site.workshop_date }}**, co-located with [ACM IMC 2026](https://conferences.sigcomm.org/imc/2026/) in Karlsruhe, Germany. The exact room is still TBD and will be announced ahead of the workshop.

Attendance is handled through the standard [IMC 2026 registration](https://conferences.sigcomm.org/imc/2026/registration/) process.
NewGeo is also listed among the [IMC 2026 co-located events](https://conferences.sigcomm.org/imc/2026/events/newgeo/).

The workshop welcomes participation from academic researchers, network operators, geolocation data providers, RIR staff, Internet standardization contributors, and policymakers.

## Contact {#contact}

For questions about the workshop, please contact the chairs:
[Oliver Gasser](mailto:oliver@ipinfo.io) and [Robert Beverly](mailto:rbeverly@sdsu.edu).
