###### [SFU AtoM Implementation Guidelines](../README.md) `>` [Archival description](overview.md) `>` [Dates of creation area](overview.md#dates-of-creation-area)

# Dates of creation area [RAD 1.4]
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

At all levels, give at least one date entry.

For a **collection**, make two entries:
- `Event type` = Collection (dates actor collected materials): enter Actor, but leave dates empty if you do not know dates of collecting activity.
- `Event type` = Document dates (date range of the documents themselves): leave `Actor` empty.

## Actor name
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   RE    |   RE    |   RE  	|   RE  	|

Always enter at the highest level.
- When left blank, unit inherits from the parent level.

At lower levels, only enter if different than parent level.

## Event type
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

Values are governed by AtoM taxonomy (`Event types`), but used differently at different levels.

Aggregate levels (fonds, series, files):
- `Creation` (dates documents were accumulated by the fonds creator).
- `Collection` (dates documents were collected by the collector).
- `Custody` (dates materials were in the custody of the custodian).
- `Document dates` (dates of the actual documents – use only if different than `Creation` dates).

At the item level:
- Select any of the entries in `Event types` taxonomy.

**Outstanding policy issue:**
- Should Archives "clean up" item-level data relating to production credits for films that were handled as events during AIS migration?

## Place
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   NR    |   NR    |   NR  	|   NR  	|

Do not use; capture place as an [Access point](access-points.md) rather than enter here.

## Date [RAD 1.4B]
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

This is the field that will display to the public user.

Use square brackets for uncertain dates, follow RAD conventions:
- Probable: [1980?]
- Approximate: [ca 1980]
- Before: [before 1980]
- After: [after 1980]
- Decade certain: [198-]
- Decade probable: [198?]
- Century certain: [19--]
- Century probable: [19--?]

Use this field to indicate predominant dates:
- E.g. "1965-1990, predominant 1982-1988"

## Start / End
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

Enter 4-digit numbers.
- AtoM uses these number fields to search and sort on.
- By default, AtoM extract values from data entered in the `Date` field.

## Event note [RAD 1.8B8]
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   OP    |   OP    |   OP  	|   OP  	|

Use for narrative information elaborating on date
- Represents RAD note 1.8B8.

---
###### [<< Previous: Class of material specific details area](class-material-specific-details.md) `|` [Next: Phyiscal description area >>](physical-description-area.md)

---
###### Last updated: Jan 11, 2022
###### MA = Mandatory `|` RE = Recommended `|` OP = Optional `|` NA = Not applicable `|` NR = Not recommended
