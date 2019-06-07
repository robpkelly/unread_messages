# unread_messages

A quick script to list unread Thunderbird messages from the command line

(Safety not guaranteed)

## Usage

```console
$ unread_messages -h
usage: unread_messages [-h] [--db DB] [-f FORMAT] [-d DATE_FORMAT] [-t TRUNCATE_TO] [-c] [-n]

Query the Thunderbird message database for unread messages

optional arguments:
  -h, --help            show this help message and exit
  --db DB               database file
  -f FORMAT, --format FORMAT
                        row format, where each formatting key is a method call with a row formatter object `r' which
                        takes as argument a maximum field length to truncate to. Valid keys: ['attachments', 'author',
                        'body', 'datetime', 'id', 'notability', 'recipients', 'subject'] (default: {:datetime(20)}
                        {:author} {:subject})
  -d DATE_FORMAT, --date-format DATE_FORMAT
                        date format, passed to `datetime.strftime' (default: None)
  -t TRUNCATE_TO, --truncate-to TRUNCATE_TO
                        number of characters to truncate long fields to (default: 60)
  -c, --count           include summary count of unread messages (default: False)
  -n, --report-none     report if there are no unread messages (default: False)
```
