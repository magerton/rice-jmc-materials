# CV Templates

## Thanks to

Thanks to Ioannis Spyridopoulos, Nick Frazier, Margaret McKeehan, and Mark Agerton at Rice University for contributions to template.

Original template from Jason Blevins <http://jblevins.org/projects/cv-template/>

Thanks to Jacquie Frazier for helpful suggestions

## For consideration...

- Conference presentations sub-section?
- Work experience?

## Version history

- [CV Template 2.2.tex](CV Template 2.2.pdf)
    * Fix `\section` spacing so that sections on new pages don't have extra space on top
    * Add underlining possibilities with `soul` package
    * Separated Research and Teaching sections
    * Add scholarship, honors, awards section
    * Add other writing and media section
    * Updated date using `fancyhdr` package

- [CV Template 2.1.tex](CV Template 2.1.pdf)
    * Use regular LaTeX font, not tgpagella
    * Update spacing on section titles
    * Updated date only on last page
    * Show 1 vs 2 row dissertation commmittee

- [CV Template 2.0.tex](CV Template 2.0.pdf)
    * Updated with new look after Ioannis Spyridopoulos resume
    * Moved honors/awards dates to RHS to keep uniform
    * Made dissertation committee 1 row to save (a bunch of) space
    * Sub-lists under Professional Activities
    * Added some space between fields and papers/abstracts
    * Made itemize work for the resume

- [CV Template-rev2.tex](older versions/CV Template-rev2.pdf) 
    * Changed font
    * No underlines, bigger headings, cleaned-up section code
    * Fixed right alignment issue
    * Removed need for `\noindent` and replaced with a need for `\forceindent`

- [CV Template-rev1.tex](older versions/CV Template-rev1.pdf) has the following changes. See the [diff view](older versions/CV Template-rev1.diff.pdf)
    * Not sure why there are two "Research Papers" sections - the second one is removed in the attached.
    * Changed the order of the categories
        * Education 
        * Committee
        * Research and Teaching Fields
        * Teaching Experience ====> Honors
        * Honors ==== > Publications
        * Prof. Activities ====> Papers
        * Publications  ====> Teaching Experience
        * Papers  ====> Prof. Activities
        * Skills [unchanged, but I'd like to delete this if possible]
    * Skills is an unnecessary category for most applications (particularly academic ones), and ideally this section would be left out.
    * Formatting fixes
        * Removed the inconsistent space before "Skills"
        * Capitalized "Dissertation Committee" to align with other titles
        * Italicized the journal title under publications, and removed the first comma following the title (because we aren't heathens). Also made a few other changes to the citation format (author names are no longer in all caps). 
        * Set the hyperlink boxes to be hidden (because yuck, right?)
    * Added titles to the conference presentations
    * Made the "Skills" section unitemized. Because a bullet list of "C++" and "Julia" looks like padding. (Apparently this was already obvious because they were both combined into a single bullet point before.)
    * Added vertical space at the end of the heading so the difference between the heading and the main text would be more clear (only affects the second page). To prevent printing problems with this change, I also made the 
    * heading space slightly wide (now only 0.25in smaller than usual, rather than 0.5in).
    * If you know how to make the heading actually right adjusted (i.e., ending at the same margin as the rest of the document), that'd be extra awesome.

- [CV Template-rev0.tex](older versions/CV Template-rev0.pdf) and [CV_Template.doc](older versions/CV_Template.doc) are initial drafts


