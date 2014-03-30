fopdoc
======

Documentation for the Fallout 3 and Fallout: New Vegas plugin file formats. 

The Oblivion, Skyrim, Fallout 3 and Fallout: New Vegas plugin file formats are all very similar, but while there exists good documentation for [Oblivion](http://www.uesp.net/wiki/Tes4Mod:Mod_File_Format) and [Skyrim](http://www.uesp.net/wiki/Tes5Mod:Mod_File_Format), there is no equivalent for Fallout 3 and Fallout: New Vegas. The aim is for this repository to become that equivalent.


### Format & Structure

This documentation is written in GitHub Flavored Markdown and stored in a Git repository on GitHub because:

* Revision control is good.
* You can download the documentation for offline reading.
* Markdown gives readable plain text and can also be readily converted to HTML.
* GitHub offers in-browser editing and HTML preview for Markdown.
* GitHub makes it easier to make, share and integrate edits with others.

The Fallout 3 documentation is stored in the [FO3](FO3) folder. Information about common data structures is stored there, and each record type gets its own file in the [FO3/Records](FO3/Records) folder.

Fallout: New Vegas likely shares many of the same data structures, so to avoid repitition reference should be made back to the FO3 docs and only differences written out in full.


### File Format Data Source

The most complete open-source implementation of plugin parsers for these games is [TES5Edit](https://code.google.com/p/skyrim-plugin-decoding-project/), written in Delphi. The information on the file formats contained within its parsing code will be adapted into a reasonably generic format that programmers should be able to interpret regardless of their preferred language, similar to how it is presented by [UESP.net](http://www.uesp.net/wiki/Tes5Mod:Mod_File_Format).

The FO3 definitions in TES5Edit are found [here](https://code.google.com/p/skyrim-plugin-decoding-project/source/browse/TES5Edit/trunk/Delphi+XE/wbDefinitionsFO3.pas). [This page](https://code.google.com/p/skyrim-plugin-decoding-project/wiki/DecodingRecords) may be useful in understanding the code.


### Contributing

I'm unfamiliar with Delphi / Pascal, so extracting the information is slow work. Anyone who's willing to help out is very welcome to: just fork the repository, and feel free to open issues on its issue tracker if you want to discuss something. You don't even need to leave your web browser, since the files can be edited and previewed on GitHub.
