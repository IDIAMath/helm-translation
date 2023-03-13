# helm-translation 

This repository holds the xml files of moodle questions from the [HELM workbooks](https://www.lboro.ac.uk/departments/mlsc/student-resources/helm-workbooks/) with the translations of the texts produced as part of the IDIAM project.

The xml files are located in subfolders, according to the chapters.


## Tools

### prettify html within xml
There is one script (with gui): `pretty_gui.py` .
The scripts formats moodle XML files and especially the HTML snippets (CDATA) inside more nicely without breaking moodle compatibility.
Specifically, the HTML tags are now formatted line-by-line, so that a version control system like GIT (which normally operates line-by-line) can handle it better.
This makes it easy to see in a diff which changes in HTML (for example translations) have been made.

### split exported xml
There is one script for cli usage: `split_exported_xml.py`.
It takes an moodle xml file with many questions (export from question bank) and outputs a separate xml file for every question in the folder `separate_questions`
