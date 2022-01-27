###### [SFU AtoM and Archival Processing Guidelines](../README.md)

# Online AtoM Import App
The [Online AtoM Import App](https://sfuarchives.shinyapps.io/atom_import/) is a web application written in `R` by Kelsey Poloney and hosted on the Archives' `shinyapps` site. It takes a custom `csv` import template listing archival materials (typically at the `file` or `item` level) and transforms it into a standard `AtoM csv import file` ready for upload to AtoM.
- There are separate, somewhat different templates for SFU Archives and SFU Special Collections.
- The app allows you to add new templates by providing an interface to map your custom template's column to AtoM fields (see [Add new templates](#add-new-templates) below).

**Contents:**
- [How to use the online app](#how-to-use-the-online-app)
- [Guide to the SFU Archives' standard template](#guide-to-the-sfu-archives-standard-template)
- [Add new templates](#add-new-templates)

**Downloads:**
- [SFU Archives Standard AtoM Import template (Excel)](../downloads/sfu-archives-standard-import-template.xlsx)

**Code and developer documentation:**
- [GitHub developer page (Kelsey Poloney](https://github.com/kpoloney/atom_import_template)

## How to use the online app
1. Download the [SFU Archives AtoM Import Template (Excel)](../downloads/sfu-archives-standard-import-template.xlsx).
- Contact SFU Special Collections for the Special Collections template.
2. Complete the template.
- It is mainly intended for listing `files` or `items` but can also be used for `series`.
3. Save the file as `csv`.
4. In any web browser, open the online app at https://sfuarchives.shinyapps.io/atom_import/.
5. Under `Institution` select "SFU Archives" (or "SFU Special Collections").
6. Under `Upload Description` click the `Browse` button and navigate to / select the csv file you saved in step 3.
7. When upload is complete, a `Download` button appears; click to create and download the data as a `AtoM csv import file`.
8. Open the SFU AtoM production site, log in, and navigate to `Import` > `CSV`.
9. On the `Import CSV` page, use the following settings (these are the defaults, they do not need to be changed):
- `Type` = "Archival description"
- `Update behaviours` = "Ignore matches and create new records on import"
- `Skip matched records` = UNCHECKED
- `Do not index records` = UNCHECKED
- Use the `Select file` button to navigate to / select the csv file you created in step 7.

AtoM will import the data and create new description records linked to their existing parent AtoM records.

**It is critical that all descriptions listed on your import template ALREADY have parent records in AtoM.**
- Make sure the `fonds` and all `series`, `sub-series`, and `sub-sub-series` already exist in AtoM before importing `files`.
- Import all `files` before you import `items`.
- You cannot for example include both `files` and their child `items` on the same import `csv` file (as you can with the standard `AtoM csv import file`).

## Guide to the SFU Archives import template
[You can download the template here.](../downloads/sfu-archives-atom-import-template.xlxs) The template is an Excel document with 2 tabs. The `Taxonomies` tab contains lists of controlled terms that generate the drop-down lists on the `FilesItems` tab.

### FilesItems tab
The `FilesItems` tab is for listing `files` and `items`.
- You can also use it for `series` but in that case a number of the columns will not apply and should be left blank; see below, [Use the template for series](#use-the-template-for-series).
- **Do not delete or edit the grey-out `Ref code`: it is a calculation field that generates the unit's full reference code.**

`Fonds`, `Series`, `Sub[series]`, `SubSub[series]` columns (A-D)
- Enter the reference number.
- Enter `0` if not applicable; **do not leave blank**.

`File`, `Item` columns (E-F)
- Enter the reference number.
- `Item` can be left blank if not applicable.

`Ref code` (G)
- **Do not edit this field (greyed out):** it is a formula that returns the unit's full reference code.

`Title` (H)
- Enter `file` / `item` title.
- Do not use square bracket for supplied titles; you can add a title note in column O if desired.




### Taxonomies tab

## Add new taxonomies


###### Last updated: Jan 20, 2022
