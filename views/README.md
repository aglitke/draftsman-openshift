# Draftsman

Draftsman is a digital tap lister designed for flexible and easy deployment
into varied beer serving environments.  The tap list can display on flat screen
monitors above a bar or on tablet devices.  The draft list is managed in a
shared Google Spreadsheet which means your display devices need only an
internet connection to display the latest updates in real time.

# Getting started

To deploy this software you need to set up a public Google spreadsheet and get
an API key for the Google sheets API.

To get an API key follow the instructions
[here](https://developers.google.com/sheets/guides/authorizing#APIKey).

Next you will want to set up a public Google spreadsheet.  You can make a copy
of [this](https://docs.google.com/spreadsheets/d/1Qv2ogP9QTMqpZGdoYKa7PJyqr1Th7Qf-z-GCkeLGzlc)
one.  Feel free to add, remove, and edit rows.  Adding new states, glassware,
and, beer colors currently requires changes to the code and/or image resources.

Make this project available to your web server or you can run a simple server
by running the following:
```
python -m SimpleHTTPServer 8000
```

To display the tap list on your device, open a web browser to
```
http://<ip>:8000/?key=<YOUR-API-KEY>&sheet=<SHEET-ID>
```
SHEET-ID is the UUID in the URL when visiting your spreadsheet (eg.
1Qv2ogP9QTMqpZGdoYKa7PJyqr1Th7Qf-z-GCkeLGzlc).
