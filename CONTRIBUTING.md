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
