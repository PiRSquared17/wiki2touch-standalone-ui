# Brief #
  * Download a MediaWiki articles dump.
  * Index it with an indexer.
  * Upload it to your iPhone/iPod touch.

# Details #

**Download a MediaWiki articles dump.**

A dump of artilces contains all textual information and description of images.

The key issue here is to find the correct file to download. Sites like Wikipedia provides dumps in various forms for different purposes, some of which contains far more data than what you need. You only need the one **"contains current versions of article content"**, i.e. pages-articles.xml.bz2.

To download wikipedia dumps, please refer to instructions in the following link:

> http://download.wikimedia.org/backup-index.html

Wiki sites based upon Wikia also use MediaWiki systems, and you can access the dump through the Special:Statistics page of that wiki. (Refer to http://www.wikia.com/wiki/Wikia:Database_download)

**Index it with an _indexer_**

The purpose of an Indexer is to scan the .bz2 file, re-arrange the content out of the xml data, and generate another file named 'articles.bin' and optionally 'images.txt' which contains the names of images.

The command is simple:

> indexer your\_dump\_file.xml.bz2

And you get articles.bin in the same folder. Note that this command will overwrite the file with the same name without warning, so use with care if you have already got an 'articles.bin' in that folder.

Other tools also provides similar functionality, and a more user-friendly GUI interface.

**Upload it to your iPhone/iPod touch**

Currently, wiki2touch is only available for jailbroken iPhoneOS devices (as well as WinCE port, which will not be discussed here). Therefore it is assumed that you are able to get access to the filesystem.

The default location is '/var/mobile/Media/Wikipedia/**xx**/', where '**xx**' stands for two-character language code, e.g. 'en' for English, 'fr' for French, 'de' for German, 'zh' for Chinese, 'ja' for Japanese, etc.

The Wikipedia in English are as large as 5GBytes, others are about hundreds of MBytes. SCP through Wifi might be slow. Some software can transfer your files through USB/dock, e.g. iFunBox on PC or DiskAid on Mac.

If with doubt, try to upload a smaller one for testing, first. A sample of articles.bin (generated from the Forgotten Realms Wiki, http://forgottenrealms.wikia.com/ ) can be found in the following URL:
> http://wiki2touch-standalone-ui.googlecode.com/files/articles.bin