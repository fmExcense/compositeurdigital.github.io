# Real estate selector

Use this type of content to display a search interface to look up real estate offers (e.g. apartments).

## Use in Compositeur Digital

With a real estate selector you can:
- choose your search criteria: surface, pric, room count, etc.
- Start a search with your criteria
- Open a result in Compositeur Digital (e.g. floor plan)

![Aperçu du module de recherche](img/immo_preview.jpg)

## Content Management

- Folder extension: `apartments`
- Expected file in the folder: `_list.csv` 

The folder contains:
- All content relative to the offers (typically floor plans of apartments).
- A spreadsheet table containing a set of descriptions that will serve as search criteria. This document is a CSV file (using `;` as delimiter) editable with spreadsheet software such as Microsoft Excel.

Here is the table tha produces the sample above:

![Aperçu du fichier _questions.csv](img/immo_csv.jpg)

### Table format

- 1st line: criteria type
- 2nd line: criteria name
- following lines: one per offer

### Criteria types

- `id`: This column is mandatory and must match a document name in the folder. It will not display as a criteria but will be used to open a result.
- `floor`: floor level.
- `type`: room count
- `surface`: surface of the residence, or of a part of it (balcony, parking space, etc.). Type in the value in m² without unit.
- `price`: Price. Multiple price columns can be defined.
- `multiple`: free criteria where multiple selection is possible.
- `single`: free criteria for which a single choice must be selected.
