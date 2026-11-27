# Structure

| Folder | What it holds |
| --- | --- |
| `constitution/` | The Constitution of the Independent State of Papua New Guinea |
| `acts/<year>/<NNN>-<slug>/` | An Act of the National Parliament (or an earlier Act or Ordinance in force), by its year and number, e.g. `acts/1997/010-companies/` is the Companies Act 1997 (No. 10 of 1997); `acts/<year>/<slug>/` when the number is not known (e.g. a Revised Laws chapter) |
| `subsidiary/<year>/<slug>/` | Regulations and Rules of Court, by year, e.g. `subsidiary/1983/national-court-rules/` |

Each folder holds one file per section (`s-012.md` is section 12, `s-012a.md` section 12A) and per schedule
(`sched-1.md`), and a `README.md` with the source and the section headings. Rules of Court arranged in Orders have one
file per Order (`order-04.md`). A text whose sections could not be split is one `text.md`. No folder holds more than
1,000 entries.

## Dates

Each version is one commit, dated 12:00 Pacific/Port_Moresby on the day it took effect, which its `In-force:`
trailer repeats. `In-force-basis:` says where that day comes from:

- `commencement`: the day the Act itself fixes;
- `certification`: the day the Speaker certified the Act (the Parliament's record), when it fixes no other day;
- `secondary-record`: the day WIPO Lex or FAOLEX records, when the copy prints no day of its own;
- `consolidation-date`: the day to which a consolidated text is brought, as its publisher records it;
- `rules-committee-notes`: for Rules of Court, the latest commencement day the Rules Committee's notes give;
- `copy-date`: for a consolidated text with no consolidation day, the day the publisher's PDF was made: the text
  as in force on that day, as printed.

An Act whose commencement is left to a notice that is not online, or with no reliable day, is held, not dated. Before
1970, which git cannot store, commits are dated 1 January 1970 with the real day in `In-force:`. No date in this
repository is the day we downloaded anything.

## Sources and tags

Official copies (Parliament, Judiciary, State bodies) come first. Copies from WIPO Lex and FAOLEX carry
`Source-status: secondary copy (...)`. Only PDFs with a text layer are used, and no OCR is run by us; a text layer the
publisher made from a scan carries `Text-source: publisher OCR`. Consolidated texts are credited to their publisher
(`Kind: publisher`); Acts as made, to the Act (`Kind: enactment`).
