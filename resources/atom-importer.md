###### [SFU AtoM Guidelines and Processing Resources](../README.md)

# AtoM Importer
###### Last updated: Jun 22, 2023
The Archives typically requires only minimal description at the **file** and **item** levels – simple lists giving only `Reference code`, `Title`, `Dates`, `Access status`, and `Container number`. It is time-consuming to enter these lists manually in AtoM, record-by-record. As an alternative, you can create a file or item list using an Excel import template and import it to AtoM. You can also use import templates for fuller series descriptions or to update / overwrite existing AtoM descriptions at any level.

There are two import templates: the [Standard AtoM import template](#standard-atom-import-template) and an [SFU-specific custom template](#sfu-archives-custom-import-template). In both cases, you work on an Excel spreadsheet and save it as csv for upload.

## Downloads / links
- [Standard AtoM import template](../downloads/atom-import-template.xlsx) = `atom-import-template.xlsx`
- [SFU custom import template](../downloads/sfu-atom-import-list.xlsx) = `sfu-atom-import-list.xlsx`
- [SFU field mapping file](../downloads/sfu-atom-import-mapping.xlsx) = `sfu-atom-import-mapping.xlsx`
- [Online AtoM Import Converter app](https://sfuarchives.shinyapps.io/atom_import/)

## Which import template to use?
The Archives initially used its own custom template, but increasingly uses the standard template as it results in a simpler process. The SFU custom template adds steps because you must also download / save a field-mapping csv file, then upload both to an online conversion app to generate a csv file ready for import to AtoM.

The main advantages of the SFU template are when / if you want to:
- Use calculation fields in the template (e.g. for reference codes).
- Use controlled vocabularies to ensure consistent data entry (drop-down menus).
- Easily set default values for specific fields.

Otherwise, it is easier to use the standard template. You can also create your own [project-specific import template](#project-specific-custom-template) in conjunction with the online conversion app.

## Standard AtoM import template
The AtoM import template is a csv file with columns for each AtoM field (80+ columns). Once completed, it can be uploaded directly to AtoM. SFU has adapted it as an Excel file, with separate tabs for `Series`, `Files` and `Items`, deleting columns not typically needed at a particular level of description. You can use either the full or adapted version.
- [Full AtoM csv import template (with all 80+ columns)](https://wiki.accesstomemory.org/Resources/CSV_templates) - from the AtoM documentation site.
- [SFU adaptation (Excel)](../downloads/atom-import-template.xlsx) - includes guidelines to column data-entry.

1. Create your series / file / item list.
- If using the SFU adaptation, use the appropriate tab and save that tab as csv.
- If using the full AtoM csv template, you can just delete any columns not required.
2. Open the csv file with BBEdit and change the settings for character encoding and line endings:
- `Character encoding` = Unicode (UTF-8)
- `Line endings` = Unix (LF)
3. Open the SFU AtoM production site, log in, and navigate to `Import` > `CSV`.
4. On the `Import CSV` page, use the following settings (these are the defaults, they do not need to be changed):
    - `Type` = "Archival description"
    - `Update behaviours` = "Ignore matches and create new records on import"
    - `Skip matched records` = UNCHECKED
    - `Do not index records` = UNCHECKED
    - Use the `Select file` button to navigate to / select the csv file you created in step 6.

AtoM will import the data and create new description records linked to their existing parent AtoM records.

### Notes
Always enter a unique value in the `legacyID` column: simplest is to use serial numbers, `1, 2, 3, 4 ...`

Do not rename or re-order column headers; it is ok to leave columns blank or delete columns not required.

Always create the `fonds` record manually in AtoM before importing any lower-level descriptions.

Always upload `series` before `files` and `items` to ensure the child descriptions link to the parent series.
- It is fine to include `series` and child `sub-` and `sub-sub-series` on the same tab.
- It is fine to include `files` and child `items` on the same tab.
- Do not include `series` and `files/items` on the same tab.

All entries on the import template **must be linked to a parent description**; how to do this depends on whether the parent describe does or does not already exist in AtoM.
- **If the parent already exists in AtoM** (e.g. you are importing files and the `series` records already exist in AtoM): enter the parent's reference code (all lowercase) in the `qubitParentSlug` column cell (e.g. `f-318-1-1`); leave the `parentID` cell blank.
- **If the parent does NOT already exist in AtoM** (e.g. you are importing `files` and their child `items` on the same csv document): use the `legacyID` value from the parent description in the `parentID` column cell and leave the `qubitParentSlug` cell blank.

See [AtoM documentation](https://www.accesstomemory.org/en/docs/2.7/user-manual/import-export/csv-import/#csv-import) for more information on the AtoM csv import process.

## SFU Archives custom import templates
The [SFU custom import template](../downloads/sfu-atom-import-list.xlsx) (`sfu-atom-import-list.xlsx`) must be used in conjunction with a [field-mapping  file](../downloads/sfu-atom-import-mapping.xlsx) (`sfu-atom-import-mapping.xlsx`).
- The import template includes separate tabs for listing `series`, `files`, and `items`, as well as a tab for `taxonomies` (controlled terms used on the other data in the form of drop-down menus).
- The mapping file lists all AtoM fields in the `atom` column and gives the corresponding column name in the `origin_fields` column.

**It is critical that all descriptions listed on your import template ALREADY have parent records in AtoM.**
- Make sure the `fonds` and all `series`, `sub-series`, and `sub-sub-series` already exist in AtoM before importing `files`.
- Import all `files` before you import `items`.
- Only with the `series` tab can you include both parent and child series on the same spreadsheet.

See the `Guidelines` tab on the spreadsheet for guidance on particular columns.

When data entry is complete, save the tab as a csv file.

### Save the field-mapping document
Download the Excel [Field mapping document](../downloads/atom-importer-field-mapping.xlsx). This maps the columns in your `data-entry` csv file to the corresponding AtoM field.
- It includes separate tabs for `series`, `files`, and `items`.

See below ([Field mapping guidance](#field-mapping-guidance)) for more about editing AtoM field mapppings.

Save the appropriate tab as a csv file, e.g. use `Files` for a file list, `Items` for an item list, etc.

### Adjust formatting
When saving the both Excel files as csv with a Mac, `character encoding` and `line endings` settings will need to be adjusted.
- Open the csv file in BBEdit and change these to "Unicode (UTF-8)" and "Unix (LF)" respectively.

### Use the online AtoM Import Converter app
<img align="right" width="400" src="../screenshots/atom-import-converter.png">

The [AtoM Import Converter app](https://sfuarchives.shinyapps.io/atom_import/) is a web application, written in `R` by Kelsey Poloney and hosted on the Archives' `shinyapps` site. It takes the two csv files (data-entry and field-mapping) and creates a standard AtoM csv import file ready for upload to AtoM.

Under `Institution` select "Other".

Under `Upload descriptions (csv)`, click the `Browse` button and navigate to / select your `data-entry.csv` file.

Under `Upload mapping (csv)`, click the `Browse` button and navigate to / select you `field-mapping.csv` file.

The app will create a new csv file called `atom_import.csv` and save it to your `Downloads` folder.
- Rename it if you like.
- This file is ready for upload to AtoM following the same steps above described under [Standard AtoM import template](#standard-atom-import-template).

Note that in earlier versions of the app, you could specify the institution (either SFU Archives or SFU Special Collections) and upload an institution-specific template, omitting the need to upload the `field-mapping` file.
- This is no longer supported; you must ALWAYS select "Other" as the `Institution` and upload a `field-mapping` file.

## Create custom import templates
You can adapt the SFU custom template to create your own import template as you see fit. Customization can be useful for specific projects that have specific descriptive needs (e.g. a digitization project and you want to include information about digitization specs). You can:
- Add new columns for entering data in additional AtoM fields.
- Edit existing taxonomies or add new ones on the `Taxonomies` tab.
- Add / edit default values on the `field-mapping` file.

If you add new columns to the template file:
- **Do NOT include blank spaces in the column name:** use e.g. `ScopeContent` instead of `Scope and content`.
- Update the `field-mapping` file by indicating which AtoM field the new columns map to (see below, [Field mapping guidance](#field-mapping-guidance)).

If you do not need a column on a specific template, you can simply delete it; you do not need to make any changes to the `field-mapping` file.

### Field mapping guidance
<img align="right" width="400" src="../screenshots/field-mapping.png">

If you add or revise columns in the SFU custom import template, you need to update the mapping file.

Each tab on the `field-mapping` Excel document has two columns:
- `atom` = the name of the AtoM field.
- `origin_fields` = the column name on the spread-sheet.

Any column on the `data-entry` file must be mapped to an AtoM field if it is to be imported.
- Columns intended for temporary reference and not for import can be left unmapped.
- An example is the `Note` column on the custom templates; intended only for temporary reference when later writing descriptions.

**Column names CANNOT include blank spaces.**
- Correct: `RefCode`.
- Incorrect: `Ref Code`.

To set default text that will be imported into every record:
- Enter a value in the `origin_fields` column using square brackets (`[]`) + the equals sign (`=`) + the default text (without quotation marks).
- E.g. `[=Final]` in the `descriptionStatus` row will set "Final" as the value in the `Restrictions on access` field on import.
