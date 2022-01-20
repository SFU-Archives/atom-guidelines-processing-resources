###### [SFU AtoM and Archival Processing Guidelines](../README.md)

# File / Item List Utilities

The Archives typically uses only minimal description at the **file** and **item** levels – simple listings giving only `Reference code`, `Title`, `Dates`, `Access status`, and `Container number`. It is time-consumming to enter these lists manually in AtoM, record-by-record. But AtoM's [csv import template](https://wiki.accesstomemory.org/wiki/Resources/CSV_templates), with its 80+ columns for every database field, is unwieldy for quick data entry. The Archives' preferred solution is to use its own custom Excel template for listing files / items (with a small number of columns), then transform it via script into an AtoM csv template ready for upload to AtoM.

The Archives has developed two different utilities for this purpose: the [Online AtoM Import app](online-atom-import-app.md) and the standalone desktop [Excel2AtoM FileMaker utility](excel2atom-filemaker-utility.md).

- The [Online AtoM Import app](online-atom-import-app.md) requires no specialized software and is more flexible, providing an interface that allow users to add multiple different custom templates.

- The [Excel2AtoM FileMaker utility](excel2atom-filemaker-utility.md) requires users to have FileMaker software installed on their local computers and it takes only one template (the one used by SFU Archives). But it provides some additional functionality, e.g. it calculates series' `Dates` from their child files and items and it generates pdf file folder labels ready for printing.

- Both apps will output an AtoM-ready csv import file. They use similar but different Excel templates for listing files and items; **use only the specific template designed for the specific app.**

### Online AtoM Import app
- Description / instructions (in preparation)
- Excel import template (in preparation)
- Link to online app (on the Archives' shinyapps site (in preparation)
- Developer's GitHub page

### Excel2AtoM FileMaker utility
- Descripton / instructions (in preparation)
- Excel import template + FileMaker database (in preparation)

---
###### Last updated: Jan 22, 2022
