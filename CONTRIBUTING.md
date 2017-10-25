---
layout: extra
title: fopdoc
---
Contributing to FOPDoc
======================

FOPDoc is the most thorough (and only?) documentation for the Fallout 3 & NV plugin file formats available. However, there's always more that can be added to make it more complete.

Welcome edits to FOPDoc include:

* Typo corrections.
* Corrections to incorrect or outdated information.
* Addition of new information on the data structures, including field values, newly decoded subrecords, or just more explanatory or descriptive text.

To edit FOPDoc, [fork](https://guides.github.com/activities/forking/) the repository, make your changes, then submit a pull request. Your changes will then be reviewed and merged into the repository. Feel free to open pull requests for work that is still in-progress if you want to discuss the changes you are making, just make sure to note that the changes are WIP in the pull request description.

FOPDoc is written using [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/), which GitHub renders to HTML. This means that you can edit and (pre)view FOPDoc in your browser, so you don't even need to have anything else installed.

Making edits yourself is the quickest and easiest way of getting changes made. However, if you would like to discuss something that doesn't necessarily require any edits, you can open an issue in FOPDoc's [issue tracker](https://github.com/WrinklyNinja/fopdoc/issues).

## Supplying New / Contradicting Information

If you submit a pull request for changes that supply new information, or which contradict existing information, please justify the changes by stating how they can be verified to be correct.

For example, this is bad:

> The field type of subrecord A in the WEAP record is wrong, it should be `float32`.

While this is good:

> The field type of subrecord A in the WEAP record is wrong. Creating a new weapon in the GECK and setting its value to a non-integer value, saving the plugin and examining it in a hex editor shows that it is stored as a `float32`.

If your changes cannot be verified, they may not be merged in.

Also, while decoding the structures involves a large amount of guesswork, if you make a guess that you can't back up with supporting evidence, please word or mark it as such (eg. "Probably", or "Maybe").

## Adding new files

The fopdoc site now uses GitHub's gh-pages Jekyll site builder.  Adding files is still the same as before, you simply create and edit a GitHub markdown formatted file. Jekyll will rebuild the site and create the .html file automatically.  However, this will not happen if the corresponding YAML Front Matter is missing from the header of the file.  To add links to other files use the file extension .html not .md.

### YAML Front Matter

Some Front Matter uses reserved keywords. One used is `layout:` and this must be one of the files in the `_layouts` folder. Other Front Matter may be added but the site may not use it. The second keyword is `title:` and currently says fopdoc. This can contain anything pertinent to the page such as the name of the record.

Other custom yaml From Matter can be added such as `description:` and then a brief description, or `game:` could be added to indicate the page belongs to the Fallout 3 record definitions. Anything can be added if there is a use for it.

However, once custom yaml Front Matter is added the corresponding layout file needs to be updated to use it and all pages will have to be updated that use that layout. If not the site won't break, you just won't see the new information on any pages without the new Front Matter.

The Front matter just needs proper yaml syntax but it needs to be in between three dashes as shown below.
```
---
layout: falloutnvrec
title: fopdoc
---
```
Once the above front matter is added Jekyll will build the proper .html file for the corresponding .md file and then you will be able to link to the file.

### Layout files

Each layout file adds specific navigation buttons.

- default: is for the main page and has a link to the xEdit site. It should not be used for other pages.
- extra: is used for files that do not belong to other records or groups pages. An example of this would be Contributing.md as it only contains information on Contributing. It has an xEdit and a Home Button.
- name-of-game + grp: Files such as fallout3grp.html is only for the Groups page as it will have specific data for Groups in the future. (subject to change)
- name-of-game + rec: Files such as fallout3rec.html is for any record definition for the corresponding game. This will be the file that should be used the most.  For Fallout NV you would use falloutnvrec.html

NOTE: The yaml Front Matter only needs the file name, not the extension of the layouts file.

If you would like to view additional Jekyll documentation please visit their [site here](https://jekyllrb.com/docs/home/).
