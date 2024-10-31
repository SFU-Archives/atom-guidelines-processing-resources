###### [SFU AtoM Guidelines and Processing Resources](../README.md)

# AtoM Import Template
###### Last updated: Oct 31, 2024
The Archives typically requires only minimal description at the **file** and **item** levels – simple lists giving only `Reference code`, `Title`, `Dates`, `Access status`, and `Container number`. It is time-consuming to enter these lists manually in AtoM, record-by-record. As an alternative, you can create a file or item list using an Excel import template and import it to AtoM. You can also use the template for fuller series descriptions or to update / overwrite existing AtoM descriptions at any level.

The [Standard AtoM import template](https://wiki.accesstomemory.org/Resources/CSV_templates) is available from Artefactual's AtoM documentation site. This contains all AtoM's 80+ fields as columns in a csv file. The Archives has created an [Excel adaptation](../downloads/atom-import-template.xlsx) with separate tabs for **series**, **files** and **items** deleting columns not typically needed at a particular level of description and providing guidance for data entry. You can use either the full or adapted version.
- [Standard AtoM csv import template](https://wiki.accesstomemory.org/Resources/CSV_templates)
- [SFU adaptation (Excel)](../downloads/atom-import-template.xlsx)

Note that from 2021-2024 the Archives also had an online conversion app to transform an SFU-specific Import template (Excel) to the standard AtoM csv. This was retired in 2024, as the Archives shifted to a simpler import process using the current adaptation of the AtoM import template.

## Use the SFU Excel template
1. Create your series / file / item list on the appropriate tab.

2. From the tab you want to import, save the file as csv (csv file will only include data from that tab).

3. Open the csv file with BBEdit and change the settings for character encoding and line endings:
- `Character encoding` = Unicode (UTF-8)
- `Line endings` = Unix (LF)

4. Open the SFU AtoM edit site and log in.

5. In the `AtoM header bar` select `Import` > `Validate CSV`.

6. Test your import csv file (`Type` = "Archival descrption").
- If there are errors, make corrections on the csv file and re-test until there are no errors.

7. In the `AtoM header bar` select `Import` > `CSV`.

8. On the `Import CSV` page, use the following settings (these are the defaults, they do not need to be changed):
    - `Type` = "Archival description"
    - `Update behaviours` = "Ignore matches and create new records on import"
    - `Skip matched records` = UNCHECKED
    - `Do not index records` = UNCHECKED
    - Use the `Select file` button to navigate to / select the csv file you created in step 6.

AtoM will import the data and create new description records linked to their existing parent AtoM records.

## Notes
Always enter a unique value in the `legacyID` column: simplest is to use serial numbers, "1, 2, 3, 4 ..."

Do not rename or re-order column headers; it is ok to leave columns blank or delete columns not required.

Always create the **fonds** record manually in AtoM before importing any lower-level descriptions.

Always upload **series** before **files** and **items** to ensure the child descriptions link to the parent series.
- It is fine to include **series** and child **sub-** and **sub-sub-series** on the same tab.
- It is fine to include **files** and child **items** on the same tab.
- Do not include **series** and **files/items** on the same tab.

All entries on the import template must be linked to a parent description; how to do this depends on whether the parent description does or does not already exist in AtoM.

**If the parent already exists in AtoM:**
- E.g. you are importing **files** and the **series** records already exist in AtoM.
- Enter the parent's reference code (all lowercase) in the `qubitParentSlug` column cell (e.g. `f-318-1-1`).
- Leave the `parentID` cell blank.

**If the parent does NOT already exist in AtoM:**
- E.g. you are importing **files** and their child **items** on the same csv document.
- Use the `legacyID` value from the parent description in the `parentID` column cell.
- Leave the `qubitParentSlug` cell blank.

See [AtoM documentation](https://www.accesstomemory.org/en/docs/2.8/user-manual/import-export/csv-import/#csv-import) for more information on the AtoM csv import process.
