# Ancestry Tools

## Documentation for [Extract](README_extract.md)

## Documentation for [Refactor](README_refactor.md)

These tools were primarily developed out of frustration at having no way of backing up many years worth of genealogy work hosted on Ancestry.com and secondarily with the lack of some basic tools on Ancestry.com.

On the first front, while a Gedcom can be downloaded most of the source citation information is not included. There is no way to download the source images being cited from or attached media items contributed by other users. You do have the option of purchasing MacKiev FamilyTree Maker or RootsMagic and use a Windows or Apple based operating system. And even then that possibly does not include copies of text only database records. 

On the second front, while Ancestry.com is a wonderful resource for records research, the site is incredibly lacking in the basic tools needed for properly maintaining an online tree. The lack of basic descendant, ahnentafel, and pedigree reports after all these years is mind boggling as is the inability to generate a fan chart. The lack of tools or at least reports to help identify potential data issues in a tree... the inability to centrally review and cleanup place names... all this from one of the largest and most successful genealogy companies in the world makes no sense.

So these utilities attempt to fill the gap somewhat by backing up as much of a tree as possible, and also help reformat the data for import to another program such as Gramps where proper reports and data management can be done.

The ancestry_extract.py utility handles all aspects of downloading the information associated with the tree from Ancestry.com  The ancestry_refactor.py utility then refactors the Gedcom file to reference the downloaded media and to fold in a lot of the extracted information that is not included in the Ancestry.com generated Gedcom. Information about both of these is included in separate readme files. The dump script simply makes viewing the raw Gedcom data easier.

Note these were written and are used on a Fedora workstation with Python 3.7.5 and Firefox 70. A virtual environment was setup, see requirements.txt for the required package list. You also need the Geckodriver for Firefox installed somewhere in your path. 

A shout out to neRok00 for the approach of querying the media API to get the authorized download link, it helped streamline things a bit as originally I was going to use the browser to do it and then pull the file out of the downloads directory.

Note these have only been used on the US version of the Ancestry.com site. I am not sure if they will work with international versions, links probably need to be edited. I do believe that Ancestry.com does prohibit tools like this now in their updated Terms and Conditions. While I should hope they do not take issue with the use of tools like this for managing your own family research, it is something to keep in mind.
