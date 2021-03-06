MonkeyScan
==========

Barcode scanning app for [MonkeySpace](http://monkeyspace.org) in Boston; works with the barcodes generated by iOS 6 PassKit as well as the official tickets generated by [guestlistapp.com](http://guestlistapp.com).

It stores all scans and attendees in a local SQLite database, and attempts to sync up with other devices at the same event via Azure Mobile Services. For now this sync'ing is manually triggered and best-effort; some work is required on the error/retry mechanism.

A scan result (failed in this case) looks like this:

![screenshot](https://raw.github.com/conceptdev/MonkeySpace/master/Screenshots/MonkeyScan/01_scan_377x695.png "Scan result")

The other screens of the app are shown below:

![screenshot](https://raw.github.com/conceptdev/MonkeySpace/master/Screenshots/MonkeyScan/00_all_500x239.png "Screenshots")

The app uses Xamarin's Windows Azure Mobile Services [component](https://components.xamarin.com/view/azure-mobile-services/) for iOS. You'd need to establish an account on [windows.azure.com](http://windows.azure.com) and create `ConfScan` and `ConfAttendee` tables for this bit to work. Also - check the code - some Azure functionality is currently commented out!

Finally, there's a feature where the scan-data can be saved/exported as a CSV to the iTunes-accessible Documents folder on your device, which you can then download for review/reporting.

Some awesome icon art from [glyphish.com](http://glyphish.com).

### Deprecated ###

**Older** versions (the one used in 2012) used [@chknofthescene](http://twitter.com/chknofthescene)'s [port of zxing](https://github.com/chkn/zxing.MonoTouch) for the barcode scanning. There are other [ports available](https://github.com/Redth/ZxingSharp.Mobile) ([@redth](http://twitter.com/redth)).
