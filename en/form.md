# Fill-in forms

Use fill-in forms to gather information from users with a simple survey form. All answers will be stored on the computer. 

## Use in Compositeur Digital

With fill-in forms, you can:
- type in text fields with a physical or virtual keyboard
- toggle checkboxes to answer multiple-choice questions or select from a set of options
- press the `Save` button on the bottom right to save the form data on disk and clear the form

![Aperçu du formulaire](img/form_preview.jpg)

## Content management

- Folder extension : `form`
- optional '_background' image file for customizing the form appearance
- form description file in the folder: `_questions.csv`

The form description file in a CSV file (*comma-separated values* with `;` as delimiter): it is editable with a sreadsheet application such as Microsoft Excel.
This file contains the list of questions that will appear in the form, each line representing one question.

Here is a sample file the produces the form above:

![Aperçu du fichier _questions.csv](img/form_csv.jpg)

### Line format:

- 1st cell: question type
- 2nd cell: question text
- following celles: available answers for multiple choice question

### Question types

- `text`: text entry with the physical or virtual keyboard
- `single`: select only one choice from the possible answers
- `multiple`: select multiple answers from the list

### Results

Results are savec on disk in the `Documents \ Compositeur Digital Form` folder.	
In this file a line with all the selected answer is added each time the `Save` button in pressed on the form.

[Back to supported types](content_types.md)
