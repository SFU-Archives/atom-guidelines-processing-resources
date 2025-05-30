###### [SFU AtoM Guidelines](../README.md) `>` [Archival description](overview.md) `>` [Dates of creation area](overview.md#dates-of-creation-area)

# Dates of creation area [RAD 1.4]
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

At all levels, give at least one date entry.

For a `collection`, make two entries:
- `Event type` = Collection (dates actor collected materials): enter Actor, but leave dates empty if you do not know dates of collecting activity.
- `Event type` = Creation (date range of the documents themselves): leave `Actor` empty.

## Actor name
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   IA    |   IA    |   IA  	|   IA  	|

Always enter at the `fonds` level for the date of creation (but can be left blank for `collections`).
- Use at lower levels only if `Creator` is different than for the fonds as a whole.
- When left blank at lower levels, unit inherits from the parent level.

## Event type
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   MA    |   MA    |   MA  	|   MA  	|

Values are governed by AtoM taxonomy (`Event types`):
- `Creation` = dates of the documents.
- `Accumulation` = dates documents were accumulated by the fonds creator
- `Collection` = dates documents were collected by a collector.
- `Custody` = dates materials were in the custody of the custodian.

`Creation` vs `Accumulation`
- Only use `Dates of accumulation` if they are different than `Dates of creation`, e.g. a donor's research files from the 1990s that contain documents or copies of documents dating back to the 1800s.
- Use the `Event note` field to explain the difference between the dates.

Note that there is a large volume of item-level legacy data for the Archives:
- Item level data relating to production credits for films were handled as events during AIS migration.

## Place
| Fonds 	| Series 	| Files 	| Items 	|
|:-----:	|:------:	|:-----:	|:-----:	|
|   DN    |   DN    |   DN  	|   DN  	|

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

Use for narrative information elaborating on date, especially where dates of accumulation and dates of document creation are different.
- Represents RAD note 1.8B8.

`Records were accumulated between 1963 and 2021 but include (in series X-X) some older original documents that date back to <<DATE>>.`

`Date of accumulation reflects the dates of record-keeping, i.e. the dates files opened / closed.`

`Files include copies of records that Evans obtained from various repositories. Dates of creation reflect the dates of the originals.`

---
###### [<< Previous: Class of material specific details area](class-material-specific-details.md) `|` [Next: Phyiscal description area >>](physical-description-area.md)

---
###### Last updated: Oct 31, 2024
###### MA = Mandatory `|` RE = Required for full description `|` IA = Required if applicable `|` OP = Optional `|` NA = Not applicable `|` DN = Do not use
