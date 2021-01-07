# SLCB Export Helper

This script allows the user to export Quote, Extra Quote, and Queue data to CSVs either
via using the added $export paremeter that comes with this script or by going to the script 
properties and trigger the export by clicking on the corresponding buttons.

## Installing

This script was built for use with Streamlabs Chatbot.
Follow instructions on how to install custom script packs at:
https://github.com/StreamlabsSupport/Streamlabs-Chatbot/wiki/Prepare-&-Import-Scripts

Click [Here](https://github.com/Encrypted-Thoughts/SLCB-ExportHelper/releases/download/v1.0/ExportHelper.zip) to download the script pack.

## Use

Once installed the below parameter can be inserted into custom commands created in SLCB.
```
$export(
    (quotes|extraQuotes|queue),   # Export Type: Specify whether to post the message to stream or to discord
    number,                       # Start Index: Set the 1 based index of the selected export type from which to begin with the export.
    string,                       # End Index: Set the 1 based index of the selected export type from which to end the export at.
                                    Note: Instead of a number enter "max" if you wish to export entire list. See examples below.
    string                        # File Name: The name of the csv file to be genered. Just put the name and do not put ".csv" at the end.
)

Example Command: !command add !exportAllQuotes $export(quotes,1,max,QuotesExport)
Example Command: !command add !exportTop5Quotes $export(quotes,1,5,Top5QuotesExport)
Example Command: !command add !exportAllExtraQuotes $export(extraQuotes,1,max,ExtraQuotesExport)
Example Command: !command add !exportAllQueue $export(queue,1,max,QueueExport)
```

Or run exports from script settings:

![buttons](https://user-images.githubusercontent.com/50642352/103844956-ad545600-5060-11eb-94bb-78a757ba8c25.png)

## Author

EncryptedThoughts - [Twitch](https://www.twitch.tv/encryptedthoughts)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

