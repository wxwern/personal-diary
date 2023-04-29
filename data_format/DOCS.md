# Raw Data Archive Format

This page describes Personal Diary's Raw Data Archive (.zip) file's data format.

You are free to make your own helper scripts that convert third-party app data to and from this format, or look for verified conversion scripts [here](https://github.com/wxwern/personal-diary/tree/master/data_format/conversion). (Consider contributing them as well!)

**Personal Diary v3.0+**

The **Raw Data Archive** import or export file must be a `.zip` file, that when unzipped, is made up of the following folder structure:

```
<journal folder>/
 |
 |-- "yyyymmdd hhmmss.ssss ZZZZ"/
 |      |--  "diary_data.txt" / "diary_data.rtf"
 |      |--  "diary_settings.json"
 |      |--  <attachment 1>
 |      |--  <attachment 2>
 |      |--  ...
 |
 |-- ...
```

A single archive contains information for a single journal. Multiple journals must be in separate archives.

Terms wrapped in `<>` are placeholders and should work with any name, while terms wrapped in `""` are required name or name formats.

Note that only image attachments are officially supported in this version. Attachment names have no definite format as long as they do not conflict with internal filenames used by the app.

Notice the structure is of a folder with subfolders for each entry. The precise requirements are as follows:
- The entry folder name should indicate the entry date as `yyyymmdd hhmmss.ssss ZZZZ` (e.g., `20230101 123456.7890 +0800`).
    - This is a fallback for readability. Date and timezone information from `diary_settings.json` inside the subfolder will be used as the conclusive information.
- Inside the entry folder:
    - Either `diary_data.txt` or `diary_data.rtf` must exist, and they should contain your entry text.
        - If there is no text, you must still include a blank `diary_data.txt` file.
            - Note: RTF files with embedded images and attachments and formatting options (other than bold, italics, underline, strikethrough, links) may not be supported or editable.
    - `diary_settings.json` must exist, containing the following information:
        -   | Key | Value Type | Description |
            |-----|------------|-------------|
            | version | number \(1\) | The `diary_settings.json` format version (this is version 1). |
            | dateSecFrom1970 | number | The number of seconds since 1970-01-01 UTC, representing the date and time the entry is written on. |
            | timezoneIdentifier | string | The timezone the entry is written in as a [Time Zone Identifier](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |
            | timezoneSecFromGMT | number | The timezone offset in seconds offset from GMT where the entry is written in. This is used if `timezoneIdentifier` is invalid or contradictory. |
            | weather | emoji-string (optional) | Weather for this entry as an emoji. |
            | mood | emoji-string (optional) | Mood for this entry as an emoji. |
            | moodCanBeAutoDetermined | boolean | Whether this entry should auto-update the `mood` value when entry contents are changed. |
            | attachmentOrder | string\[\] | The list of filenames of attachments for this entry, indicating the sorted display order. |
            | tags | string\[\] | The list of tags for this entry. They should not contain spaces. |

        - For example:
            ```
            {
                "version" : 1,
                "dateSecFrom1970" : 1672547696,
                "timezoneIdentifier" : "Asia\/Singapore",
                "timezoneSecFromGMT" : 28800,
                "weather" : "⛅️",
                "mood" : "😃",
                "moodCanBeAutoDetermined" : true,
                "attachmentOrder" : [
                    "Attachment_Image_1.png",
                    "Attachment_Image_2.png"
                ],
                "tags" : [
                    "personal", "work"
                ]
            }
            ```
