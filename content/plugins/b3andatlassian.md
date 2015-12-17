---
date: 2015-05-09T16:46:35+02:00
title: "Using Mockups 3 for Desktop and Mockups for Confluence or JIRA versions together"
menu:
  menuplugins:
    parent: plugins
weight: 20
---

{{% alert warning %}}**Heads Up!** Balsamiq Mockups 3 for Desktop, at the moment, uses a different file format than Mockups for Confluence and Mockups for JIRA. We plan to bring the changes in Balsamiq Mockups 3 to our Atlassian plugins soon.{{% /alert %}}

## Exporting from the desktop version 

Here's how to export your mockups from Mockups 3 for Desktop and bring them into Mockups for Confluence or JIRA:

1.  Open the project in Mockups 3 for Desktop and export it to a ZIP file using _Project > Export > Project to BMMLs ZIP_
2.  Expand the ZIP file to find the BMML files.
3.  For each mockup you want to import, do the following:
    1.  Open a BMML in your favorite plain text editor (for example Text Edit on Mac or Notepad on Windows)
    2.  Select all the text and copy it to your clipboard (CTRL+C)
    3.  Create a new mockup in Mockups for Confluence or Mockups for JIRA and use _Mockup > Import Mockup XML._
    4.  Paste (CTRL+V) and hit _Import_.
    5.  Fix any broken images by uploading the image from the ZIP (they'll be in the _assets_ folder)
    6.  Symbols are not supported in Mockups for Confluence or Mockups for JIRA yet, so you might have to recreate those as well.
    7.  Save.

We know this is a bit of an arduous process right now. We promise it will be better soon!

* * *

## My plugin version of Mockups doesn't support symbols, does that mean that I can't import mockups that use symbols?

Mockups for Confluence and Mockups for JIRA don't yet support [symbols](http://support.balsamiq.com/customer/portal/articles/110439), but that doesn't mean that you can't import mockups that use symbols.

In Balsamiq Mockups for Desktop (version 2), when you export a mockup that contains symbols ("File > Export Mockup XML" in the menu), you will see the following dialog:

![Dialog](http://media.balsamiq.com/img/support/prodfaqs/exportinbmml.png)

There are two options: **"Export As-Is"** and **"Export with Symbols 'Broken Apart'"**. Choosing the first option _will not include_ symbols in the exported XML. This is appropriate for exporting and importing between versions that support symbols (such as Mockups for Desktop and myBalsamiq).

Choosing the second option, on the other hand, will _merge_ the XML from the symbols that are used in the mockup with the XML from the mockup itself, resulting in a single file with all the controls that are shown in the mockup that is being exported. Note that the file you're working on won't be affected either way, this merging is only done for the BMML code that's placed in your clipboard. This is the option that we recommend for plugin users as an easy way to import a mockup and its symbols all at once.

* * *

## Can I copy and paste between the desktop and plugin version?

Yes! Er, well, something like that...

Let's say that you have both Mockups for Desktop (version 2) and a plugin version open and you want to copy a specific control or set of controls from Mockups for Desktop into a plugin version.

It would be great to just copy and paste, right? Well, there is a limitation in Adobe Flash that prevents copying from outside the browser into a Flash application (it's a security thing), however, you can do essentially the same thing by performing the following steps:

1.  Select the control(s) you want to copy in Mockups for Desktop and copy them (using CTRL/CMD + C or "Edit > Copy" in the menu)
2.  Switch to the plugin version (Confluence, JIRA, etc.) and go to "Import Mockup XML…" from the Mockup menu
3.  Use CTRL/CMD + V or "Paste" from the right-click menu to paste in the mockup XML that was copied from Mockups for Desktop
4.  Click the "Import" button in the dialog.

You should now see the control(s) from Mockups for Desktop in your plugin version.

* * *

## Can I download mockups created in my Atlassian plugin version for use with Mockups for Desktop?

Most of the products we integrate with make it clear where to find the mockup (.bmml) files. To download these files, just right-click on the link to the .bmml file and select "save link as…" (or whatever terminology your browser uses). Then use Balsamiq Mockups version 2 to open the BMML files or [import them](http://support.balsamiq.com/customer/portal/articles/1895737#importingbmml) if you are using Balsamiq Mockups version 3.

However, Confluence users might find it a little tricky to locate the mockup files to download. To find them, go to the page attachments by clicking "Tools > Attachments". Here, you will see two files for each mockup, one PNG image and one .bmml file. You can download the .bmml file from this list.
