# Papua New Guinea: law history in git

The law of Papua New Guinea as a git history: one file per provision, one commit per law on the day its change took effect, and the law that made each change as the commit's author. `git blame` names the law behind every line; picking a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `pg/`.

**What is in it now**

| Folder | Law | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | Constitution of the Independent State of Papua New Guinea, consolidated reprint published on the National Parliament website | 1 | Oldest version available, dated 9 October 2009 (the date of the PDF). Files: `preamble`, `heading-NNN` (parts, divisions and subdivisions, in reading order), `sec-NNN[-x]` (sections 1 to 344, with lettered sections) and `sch-01` to `sch-06` (one file per schedule) |
| `criminal-code/` | Criminal Code Act 1974 (Chapter 262), with the Criminal Code in Schedule 1, consolidated text hosted by the Independent Commission Against Corruption | 1 | Oldest version available, dated 6 November 2023 (the date of the PDF; the PDF is an undated consolidation). Files: `act-001` to `act-006` (the Act), `s-001` to `s-628` (sections of the Code; sections printed as repealed are not included) |
| `companies-act/` | Companies Act 1997 (No. 10 of 1997), consolidated text hosted by the Investment Promotion Authority | 1 | Oldest version available, dated 9 June 2026 (the date of the PDF; the file is described as consolidated to 2014). Files: `s-001` to `s-457` (letter suffixes as `s-429a`) and `sched-01` to `sched-15` |
| `employment-act/` | Employment Act 1978 (Chapter 373), text published by the Department of Personnel Management in its Employment and Industrial Relations Library | 1 | Oldest version available, dated 8 May 2019 (the date of the PDF; the Act came into force on 1 January 1981 and the PDF states no consolidation date). Files: `s-001` to `s-155` and `sched-01` (the ration scale) |

**Language.** English, the language of the Constitution.

**Limits of this first build**

- One version, credited to the publisher as "oldest version available". The Parliament publishes one consolidated reprint and no history. The date is the date the PDF was created, not an in-force date: the Constitution came into force on 16 September 1975, and amendments made after the reprint may be missing.
- The PDF's footnotes (which name the amending laws), running headers and page numbers are not reproduced.
- Paragraph breaks are read from the "(1)" and "(a)" markers and from line spacing.
- Only the Criminal Code Act 1974, the Companies Act 1997 and the Employment Act 1978 are included among the Acts so far (Papua New Guinea has no civil code; the Companies Act is the nearest commercial statute); other Acts, Organic Laws and the Bougainville Constitution are not included.

**Source.** National Parliament of Papua New Guinea, [parliament.gov.pg/constitution-of-png](https://parliament.gov.pg/constitution-of-png/), PDF read on 29 October 2026. The sha256 of the bytes it was parsed from is in `data/versions.json`. The Criminal Code comes from the Independent Commission Against Corruption, [icac.gov.pg](https://icac.gov.pg/wp-content/uploads/2023/11/Criminal-Code-Act-1974.pdf), read on 30 October 2026. The Companies Act comes from the Investment Promotion Authority, [ipa.gov.pg](https://www.ipa.gov.pg/Documentation/PG/ActsAndRegulations/Companies_Act_1997_(consolidated_to_2014).pdf), read on 30 October 2026. The Employment Act comes from the Department of Personnel Management, [dpm.gov.pg](https://www.dpm.gov.pg/wp-content/uploads/2019/01/Employment-Act-1978.pdf), read on 30 October 2026.

How these files were made is in [REPRODUCE.md](REPRODUCE.md). This repository is not legal advice and not an official publication; for anything that matters, read the original.
