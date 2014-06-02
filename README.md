FOPDoc
======

Documentation for the Fallout 3 and Fallout: New Vegas plugin file formats. 

The Oblivion, Skyrim, Fallout 3 and Fallout: New Vegas plugin file formats are all very similar, but while there exists good documentation for [Oblivion](http://www.uesp.net/wiki/Tes4Mod:Mod_File_Format) and [Skyrim](http://www.uesp.net/wiki/Tes5Mod:Mod_File_Format), there is no equivalent for Fallout 3 and Fallout: New Vegas. The aim is for this repository to become that equivalent.

### Contents

Documentation for the Fallout 3 plugin file format is found in the [FO3](FO3) folder. All records and fields have been documented to match the state of knowledge of the file format in TES5Edit as of 2 June 2014.

Documentation for the Fallout: New Vegas plugin file format has yet to be written. Much of the file format is identical to that used by Fallout 3, so to prevent unnecessary repetition only records, fields, values, etc. that differ will be documented, and the Fallout 3 documentation refered to otherwise.

### Format

This documentation is written in [GitHub Flavored Markdown](https://guides.github.com/overviews/mastering-markdown/) and stored in a Git repository on [GitHub](https://github.com/WrinklyNinja/fopdoc) because:

* Revision control is good.
* You can download the documentation for offline reading.
* Markdown gives readable plain text and can also be readily converted to HTML.
* GitHub offers in-browser editing and HTML preview for Markdown.
* GitHub makes it easier to make, share and integrate edits with others.

### File Format Data Source

The most complete open-source implementation of plugin parsers for these games is [TES5Edit](https://code.google.com/p/skyrim-plugin-decoding-project/), written in Delphi. The information on the file formats contained within its parsing code has been adapted into a reasonably generic format that programmers should be able to interpret regardless of their preferred language, similar to how it is presented by [UESP.net](http://www.uesp.net/wiki/Tes5Mod:Mod_File_Format).


### Contributing

I'm unfamiliar with Delphi / Pascal, so extracting the information is slow work. Anyone who's willing to help out is very welcome to: just fork the repository, and feel free to open issues on its issue tracker if you want to discuss something. You don't even need to leave your web browser, since the files can be edited and previewed on GitHub.

The FO3 definitions in TES5Edit are found [here](https://skyrim-plugin-decoding-project.googlecode.com/svn/TES5Edit/trunk/Delphi%20XE/wbDefinitionsFO3.pas), and the FNV definitions are found [here](https://skyrim-plugin-decoding-project.googlecode.com/svn/TES5Edit/trunk/Delphi%20XE/wbDefinitionsFNV.pas). [This page](https://code.google.com/p/skyrim-plugin-decoding-project/wiki/DecodingRecords) may be useful in understanding the code. In practice though, searching [this source file](https://skyrim-plugin-decoding-project.googlecode.com/svn/TES5Edit/trunk/Delphi%20XE/wbInterface.pas) may be more useful.
