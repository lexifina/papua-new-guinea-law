# How this repository was made (Papua New Guinea)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| National Parliament of Papua New Guinea, Constitution of PNG | <https://parliament.gov.pg/constitution-of-png/> | 2026-10-29 | No licence statement; official publication of the Parliament. |
| Independent Commission Against Corruption of Papua New Guinea, Criminal Code Act 1974 (Ch. 262) | <https://icac.gov.pg/wp-content/uploads/2023/11/Criminal-Code-Act-1974.pdf> | 2026-10-30 | No licence statement; the PDF is the Office of Legislative Counsel consolidation hosted by a State body. |
| Investment Promotion Authority of Papua New Guinea, Companies Act 1997 (consolidated to 2014) | <https://www.ipa.gov.pg/Documentation/PG/ActsAndRegulations/Companies_Act_1997_(consolidated_to_2014).pdf> | 2026-10-30 | No licence statement; the PDF is a consolidation of the Act hosted by a State body. |
| Department of Personnel Management of Papua New Guinea, Employment Act 1978 (Employment and Industrial Relations Library) | <https://www.dpm.gov.pg/wp-content/uploads/2019/01/Employment-Act-1978.pdf> | 2026-10-30 | No licence statement; official text of an Act hosted by a State body. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Constitution of the Independent State of Papua New Guinea | 1 | 2009-10-09 to 2009-10-09 |
| `criminal-code` | Criminal Code Act 1974 (Chapter 262), with the Criminal Code in Schedule 1 | 1 | 2023-11-06 to 2023-11-06 |
| `companies-act` | Companies Act 1997 (No. 10 of 1997), consolidated | 1 | 2026-06-09 to 2026-06-09 |
| `employment-act` | Employment Act 1978 (Chapter 373) | 1 | 2019-05-08 to 2019-05-08 |

The build made 4 commits:

| Commits | Kind |
| ---: | --- |
| 4 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 0 laws in the record.
- 4 tags.

## Dates

Each commit is dated at noon (Pacific/Port_Moresby) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: The Parliament publishes the Constitution as consolidated and gives no per-version dates; the version is dated by the date of the PDF reprint. https://parliament.gov.pg/constitution-of-png/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `f42640244a97d98faa4e1a89c43d6e5d4748121acbc40e15085ed0847e42da6f` (1893944 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

4 versions of 4 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

A second build from the same corpus into an empty folder gave identical hashes for all 4 history commits and 4 tags (history tip `b478653e6dc241851ee209c8e5a8f08b9691b32f`).

## Decisions made by hand

- Oldest version available: the Parliament publishes one consolidated reprint and no history, so it is one version credited to the publisher, dated 2009-10-09, the creation date of the PDF. The Constitution came into force on 16 September 1975; this is not an in-force date of the text, and amendments after the reprint may be missing.
- Footnotes (which name the amending laws), running headers and page numbers are left out.
- Section titles are kept as printed; paragraph breaks are read from line starts "(1)", "(a)" and line spacing.
- Each schedule is one file; headings of parts, divisions and subdivisions are heading-NNN files numbered in reading order.
- Criminal Code: one version dated 2023-11-06, the HTTP Last-Modified date of the ICAC PDF, credited to the publisher as "oldest version available". It is not the in-force date: the Act is of 1974 and the PDF is an undated consolidation ("Certified on: / /20 .").
- Criminal Code: the six sections of the Act itself are act-NNN and the sections of the Code in Schedule 1 are s-NNN (letter suffixes as s-NNNa). Part, division and subdivision headings, running headers, page numbers and margin section references are left out, and so are page-foot amendment notes (matched by their wording) and sections printed as "[REPEALED.]"; each section keeps its printed number and heading as its first line.
- Companies Act 1997: one version dated 2026-06-09, the HTTP Last-Modified date of the IPA PDF, credited to the publisher as "oldest version available". It is not the in-force date: the Act is No. 10 of 1997 and the file is described as consolidated to 2014.
- Companies Act 1997: one unit per section (s-NNN, letter suffixes as s-NNNa) and one per schedule (sched-NN). The nearest equivalent of a commercial code; Papua New Guinea has no civil code. Part and division headings, the arrangement of sections, running headers, page numbers and page-foot amendment notes (matched by their wording) are left out; each section keeps its printed number and heading as its first line.
- Employment Act 1978: one version dated 2019-05-08, the last-modified date of the Department of Personnel Management PDF, credited to that Department as "oldest version available". It is not the in-force date: section 1 gives the commencement date as 1 January 1981, and the PDF states no consolidation date, so later amendments may be missing.
- Employment Act 1978: one unit per section (s-NNN) and one per schedule (sched-NN). Part and division headings are left out; each section keeps its printed number and heading as its first line. Line wraps are joined into paragraphs at "(1)", "(a)", "(i)", quoted definitions and "Penalty:" lines, and where a line ending in punctuation is followed by a less indented line. Schedule tables keep their printed lines with runs of spaces collapsed.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code wrote the deterministic extraction code; no model wrote or altered any legal text.
- none
