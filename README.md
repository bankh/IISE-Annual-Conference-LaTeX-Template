# IISE Annual Conference LaTeX Template

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![LaTeX](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)

Professional LaTeX template for **IISE Annual Conference** proceedings submissions. This template is fully compliant with official IISE formatting guidelines and ready to use for your conference paper.

## 📋 Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [Template Specifications](#template-specifications)
- [Compilation Instructions](#compilation-instructions)
- [Pre-Submission Checklist](#pre-submission-checklist)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview

This LaTeX template is specifically designed for submissions to the **IISE Annual Conference Proceedings**. It ensures your paper meets all formatting requirements for conference submissions.

### Key Features

✅ **Fully Compliant** - Meets all official IISE Annual Conference formatting guidelines  
✅ **6-Page Format** - Strict 6-page limit built-in  
✅ **IEEE Citations** - Pre-configured IEEE-style citation format  
✅ **Blind Review Ready** - Author information placeholder for blind submissions  
✅ **Professional Layout** - Times New Roman throughout, proper spacing and margins  
✅ **Well Documented** - Extensive inline comments to guide your writing  

### What's Included

- `IISE Annual Conference Template.tex` - The main template file
- `IISE Annual Conference Template.pdf` - Example output
- `README.md` - This documentation
- `LICENSE` - Creative Commons Attribution 4.0 International License

## Quick Start

Get started with your conference paper in 5 minutes:

```bash
# 1. Download or copy the template
cp "IISE Annual Conference Template.tex" "my-paper.tex"

# 2. Open in your favorite LaTeX editor
# (TeXstudio, VS Code with LaTeX Workshop, Overleaf, etc.)

# 3. Update the key information:
#    - Title (line ~88)
#    - Abstract ID (line ~92)
#    - Abstract text (line ~106, max 250 words)
#    - Keywords (line ~111, 3-5 keywords)

# 4. Fill in your content in the sections

# 5. Compile twice for proper references
pdflatex "my-paper.tex"
pdflatex "my-paper.tex"
```

That's it! You now have a properly formatted IISE conference paper.

## Installation

### Prerequisites

You need a LaTeX distribution installed on your system.

#### Linux (Ubuntu/Debian)
```bash
sudo apt-get update
sudo apt-get install texlive-full
```

#### macOS
```bash
brew install --cask mactex
```

#### Windows
Download and install [MiKTeX](https://miktex.org/download) or [TeX Live](https://www.tug.org/texlive/)

#### Online Option (No Installation)
Use [Overleaf](https://www.overleaf.com) - upload the template and compile online

### Required LaTeX Packages

The template uses these standard packages (included in full LaTeX distributions):

- `geometry` - Page layout (1 inch margins)
- `times` - Times New Roman font
- `graphicx` - Figure support
- `amsmath` - Mathematical equations
- `cite` - IEEE-style citations
- `url` - URL formatting in references
- `fancyhdr` - Headers and footers
- `titlesec` - Section formatting
- `caption` - Caption formatting
- `parskip` - Paragraph spacing
- `enumitem` - Bullet list formatting

## Usage Guide

### Step 1: Basic Information

#### Update the Title

Find line ~88 and update your paper title:

```latex
{\fontsize{16}{19}\bfseries\selectfont 
Your Paper Title Goes Here}
```

#### Update the Abstract ID

Find line ~92 and add your submission ID:

```latex
{\fontsize{12}{14}\bfseries\selectfont Abstract ID: YOUR_ID}
```

#### Write Your Abstract

Replace the example abstract around line ~106 (maximum 250 words):

```latex
{\fontsize{10}{12}\selectfont
Your abstract text here. Maximum 250 words describing your research question,
methodology, key findings, and implications...
}
```

#### Add Keywords

Add 3-5 keywords around line ~111:

```latex
{\fontsize{10}{12}\selectfont
keyword1, keyword2, keyword3, keyword4, keyword5
}
```

### Step 2: Writing Your Paper

#### Adding Sections

The template includes standard sections. Customize as needed:

```latex
\section{Introduction}
Your introduction text here...

\section{Literature Review}
Review of relevant prior work...

\section{Methodology}
\subsection{Data Collection}
Details of your data collection process...

\subsection{Analysis Approach}
Description of your analytical methods...

\section{Results}
Your findings...

\section{Discussion}
Interpretation of results...

\section{Conclusion}
Summary and future work...
```

#### Adding Figures

Figures should have captions **below** them:

```latex
\begin{figure}[h!]
\centering
\includegraphics[width=0.6\textwidth]{your-figure.pdf}
\caption{Your descriptive figure caption goes here}
\label{fig:example}
\end{figure}
```

Reference figures in text:
```latex
As shown in Figure \ref{fig:example}, the results indicate...
```

**Supported formats:** PDF (preferred), PNG, JPG, EPS

#### Adding Tables

Tables should have captions **above** them:

```latex
\begin{table}[h!]
\centering
\caption{Your descriptive table caption goes here}
\label{tab:example}
\begin{tabular}{|l|c|c|}
\hline
\textbf{Column 1} & \textbf{Column 2} & \textbf{Column 3} \\
\hline
Data 1 & Data 2 & Data 3 \\
Data 4 & Data 5 & Data 6 \\
\hline
\end{tabular}
\end{table}
```

Reference tables in text:
```latex
Table \ref{tab:example} presents the comparison...
```

#### Adding Equations

Center equations and number them:

```latex
\begin{equation}
E = mc^2
\label{eq:einstein}
\end{equation}
```

Reference equations in text:
```latex
Equation \ref{eq:einstein} represents...
```

#### Adding References

Use IEEE style in the bibliography section (around line ~174):

```latex
\begin{thebibliography}{9}
\setlength{\itemsep}{0pt}
\setlength{\parskip}{0pt}

\bibitem{author2024}
A. Author, B. Coauthor, ``Paper Title,'' \textit{Journal Name}, 
vol. 10, no. 2, pp. 123--145, 2024.

\bibitem{smith2024}
C. Smith, ``Conference Paper Title,'' in \textit{Proceedings of 
IISE Annual Conference}, Orlando, FL, 2024, pp. 456--467.

\end{thebibliography}
```

**Important:** References must be numbered **in order of appearance** in the text, not alphabetically.

Cite in text:
```latex
Previous research \cite{author2024} has shown...
Multiple studies \cite{author2024,smith2024} indicate...
```

### Step 3: Acknowledgements (Optional)

Update the acknowledgements section around line ~164:

```latex
\section*{Acknowledgements}
The authors acknowledge support from [funding agency/institution]...
```

## Template Specifications

### Page Layout
- **Paper size:** US Letter (8.5" × 11")
- **Margins:** 1 inch on all sides
- **Page limit:** 6 pages maximum (strict, including all content)
- **Page numbers:** None
- **Header:** First page only (proceedings editors' information)

### Typography
- **Font family:** Times New Roman throughout
- **Title:** 16pt, bold, centered
- **Abstract ID:** 12pt, bold, centered
- **Abstract heading:** 12pt, bold, centered
- **Abstract text:** 10pt, full-justified (≤250 words)
- **Keywords heading:** 12pt, bold, left-justified (NOT numbered)
- **Keywords text:** 10pt
- **Section headings:** 12pt, bold, numbered, left-justified
- **Subsection headings:** 10pt, bold, numbered, left-justified
- **Subsubsection headings:** 10pt, bold, numbered, left-justified
- **Body text:** 10pt, full-justified
- **Line spacing:** Single (1.0)
- **Paragraph spacing:** 10pt between paragraphs, no indentation

### Elements
- **Tables:** Caption above, centered, normal font size
- **Figures:** Caption below, centered, normal font size
- **Equations:** Centered, numbered on right margin
- **References:** IEEE style, numbered sequentially by order of appearance
- **Bullet lists:** Standard bullets, properly indented

### Formatting Rules
-  No paragraph indentation (block style)
-  Single blank line (10pt) between paragraphs
-  Sections and subsections are numbered
-  Keywords section is NOT numbered
-  Acknowledgements section is NOT numbered
-  References section is NOT numbered

## Compilation Instructions

### Standard Compilation

For papers with manual bibliography (recommended for conference papers):

```bash
cd /path/to/your/paper
pdflatex "IISE Annual Conference Template.tex"
pdflatex "IISE Annual Conference Template.tex"  # Run twice for references
```

**Why compile twice?** The first run processes citations and labels, the second run populates them correctly.

### Using Latexmk (Automated)

Latexmk automates the compilation process:

```bash
latexmk -pdf "IISE Annual Conference Template.tex"

# To clean auxiliary files after compilation:
latexmk -c
```

### Using Overleaf

1. Create a new project on [Overleaf](https://www.overleaf.com)
2. Upload `IISE Annual Conference Template.tex`
3. Click "Recompile" (Overleaf automatically handles multiple passes)
4. Download the PDF when ready

### Using TeXstudio / TeXworks / VS Code

Simply click the "Build" or "Compile" button in your editor. Most modern LaTeX editors automatically run pdflatex twice.

### Common Compilation Errors

**Error: "Font shape undefined"**
```bash
# Install required fonts
sudo apt-get install texlive-fonts-recommended
```

**Error: "File not found"**
- Ensure all referenced figures are in the same directory
- Check that file names match exactly (case-sensitive on Linux/Mac)

## Pre-Submission Checklist

Before submitting your paper to the IISE Annual Conference, verify:

### Content Requirements
- [ ] Paper title is descriptive and properly formatted (16pt, bold, centered)
- [ ] Abstract ID is included and correct
- [ ] Abstract is present and ≤ 250 words
- [ ] 3-5 relevant keywords are listed
- [ ] Author information is **blank** (for initial blind submission)
- [ ] Main sections present: Introduction, Methodology, Results, Conclusion
- [ ] All claims are properly cited with references

### Formatting Requirements
- [ ] All sections are numbered correctly (except Keywords, Acknowledgements, References)
- [ ] Section headings are 12pt, bold, left-justified
- [ ] Subsection headings are 10pt, bold, left-justified
- [ ] Body text is 10pt Times New Roman, full-justified
- [ ] Single line spacing throughout
- [ ] No paragraph indentation (block style)

### Figures and Tables
- [ ] All figures have captions **below** them
- [ ] All tables have captions **above** them
- [ ] All figures and tables are referenced in the text
- [ ] Figure/table labels are descriptive
- [ ] Images are high quality and legible

### Equations and Math
- [ ] All equations are centered
- [ ] Important equations are numbered
- [ ] All numbered equations are referenced in text

### References and Citations
- [ ] All references are in IEEE format
- [ ] References are numbered **in order of appearance** (not alphabetically)
- [ ] All in-text citations have corresponding references
- [ ] All references are cited at least once in the text
- [ ] DOIs or URLs are included where available

### Final Checks
- [ ] **Total page count is ≤ 6 pages** (including title, abstract, figures, tables, references)
- [ ] No page numbers or footers appear
- [ ] First page header shows proceedings editors' information
- [ ] Document compiles without errors or warnings
- [ ] PDF has been thoroughly reviewed
- [ ] All text is readable and properly formatted in PDF
- [ ] No overfull/underfull hbox warnings (or minimal)

## Troubleshooting

### Issue: Exceeding 6-Page Limit

This is the most common issue. Solutions:

1. **Reduce figure sizes:**
   ```latex
   \includegraphics[width=0.5\textwidth]{figure.pdf}  % Instead of 0.6 or 0.7
   ```

2. **Combine related figures using subfigures:**
   ```latex
   \usepackage{subcaption}
   \begin{figure}[h!]
   \centering
   \begin{subfigure}{0.45\textwidth}
       \includegraphics[width=\textwidth]{fig1.pdf}
       \caption{First subfigure}
   \end{subfigure}
   \begin{subfigure}{0.45\textwidth}
       \includegraphics[width=\textwidth]{fig2.pdf}
       \caption{Second subfigure}
   \end{subfigure}
   \caption{Combined figure}
   \end{figure}
   ```

3. **Tighten writing** (but keep 10pt font - don't cheat!)
4. **Move supplementary material** to an appendix or supplementary document
5. **Consolidate tables** with similar information

### Issue: Bibliography Not Showing

**Solution:** Make sure you:
1. Have at least one `\cite{...}` command in your text
2. Compile **twice** - the first pass identifies citations, the second displays them
3. Have matching `\bibitem` labels in the bibliography

### Issue: Figures Not Appearing

**Problem:** "File not found" error

**Solutions:**
- Ensure figure files are in the same directory as the `.tex` file
- Check file name spelling (case-sensitive!)
- Use supported formats: PDF, PNG, JPG, or EPS
- Provide full path if figures are in a subdirectory:
  ```latex
  \includegraphics[width=0.6\textwidth]{./figures/myfigure.pdf}
  ```

### Issue: Figure/Table in Wrong Location

**Solutions:**
- Use `[h!]` for "here, definitely"
- Use `[t]` for top of page
- Use `[b]` for bottom of page
- Use `[H]` for absolute positioning (requires `\usepackage{float}`)
- Let LaTeX decide with `[htbp]` (here, top, bottom, page)

**Important:** LaTeX optimizes placement for readability. Sometimes it's better to trust LaTeX's judgment!

### Issue: Special Characters Not Rendering

Use proper LaTeX escape sequences:

```latex
\%      % Percent sign
\$      % Dollar sign  
\&      % Ampersand
\_      % Underscore
\#      % Hash/pound sign
\{      % Left brace
\}      % Right brace
\~{}    % Tilde
\^{}    % Caret
```

### Issue: Margins Look Wrong

**Solution:** Don't modify the geometry settings! They are configured to meet IISE requirements:

```latex
\usepackage[letterpaper, margin=1in, headheight=25pt]{geometry}
```

If margins still look wrong, ensure you're viewing at 100% zoom in your PDF reader.

### Issue: Citations Showing as [?]

This means LaTeX can't find the reference. Check:
1. The `\bibitem{label}` exists in the bibliography
2. The label in `\cite{label}` matches exactly (case-sensitive)
3. You've compiled twice

### Issue: Title or Abstract on Second Page

**Solution:** Your content is too long. The title, abstract, and keywords must fit on page 1. Options:
- Shorten your abstract (max 250 words)
- Reduce number of keywords
- Don't add extra spacing before sections

## Tips and Best Practices

### General Writing Tips

1. **Start with an outline** - Fill in section headings before writing
2. **Write iteratively** - Don't try to perfect everything in one pass
3. **Compile frequently** - Check formatting as you write (every 30 minutes)
4. **Use labels religiously** - Never hard-code "Figure 1", always use `\ref{fig:label}`
5. **Read the PDF** - Always review the compiled output, not just the source

### Managing Page Limits

1. **Check page count early** - Don't wait until the end
2. **Be concise** - Every word should add value
3. **Use tables and figures efficiently** - They convey information densely
4. **Prioritize content** - What's essential vs. supplementary?
5. **Save detailed derivations** for an appendix or supplementary material

### Figure Best Practices

1. **Use vector graphics** (PDF, EPS) for diagrams, charts, plots
2. **Use high-resolution raster** (PNG ≥300 DPI) for photos or screenshots
3. **Consistent style** - Same fonts, colors, line widths across all figures
4. **Readable labels** - Large enough to read when figure is sized to column width
5. **Color-blind friendly** - Use patterns or line styles in addition to colors

### Citation Best Practices

1. **Cite as you write** - Don't leave citations for later
2. **Be complete** - Include all required information (authors, title, venue, year, pages)
3. **Use DOIs** when available - Easier for readers to find papers
4. **Check accuracy** - Verify author names, publication years, page numbers
5. **Follow IEEE format** - See [IEEE Citation Guidelines](https://ieee-dataport.org/IEEECitationGuidelines.pdf)

### Version Control Tips

1. **Use meaningful file names** - `my-paper-v1.tex`, `my-paper-v2.tex`
2. **Date your versions** - `my-paper-2025-11-14.tex`
3. **Use Git** if comfortable - Track all changes systematically
4. **Backup regularly** - Cloud storage (Dropbox, Google Drive, OneDrive)
5. **Keep old versions** - You might want to revert changes

## IEEE Citation Examples

### Journal Article
```latex
\bibitem{author2024}
A. Author, B. Coauthor, ``Paper Title Here,'' \textit{Journal Name}, 
vol. 56, no. 3, pp. 123--145, Mar. 2024.
```

### Conference Paper
```latex
\bibitem{smith2024}
C. Smith, D. Jones, ``Conference Paper Title,'' in \textit{Proceedings of 
2024 IISE Annual Conference}, Montreal, Canada, May 18-21, 2024, pp. 567--578.
```

### Book
```latex
\bibitem{chang2022}
T. Chang, R. Wysk, H. Wang, \textit{Computer-Aided Manufacturing}, 
4th ed. Upper Saddle River, NJ: Pearson, 2022.
```

### Book Chapter
```latex
\bibitem{wilson2023}
M. Wilson, ``Chapter Title,'' in \textit{Book Title}, 
J. Editor, Ed. Boston, MA: Publisher, 2023, pp. 45--67.
```

### Website
```latex
\bibitem{ieee2024}
IEEE, ``IEEE Citation Guidelines,'' 2024. [Online]. 
Available: https://ieee-dataport.org/IEEECitationGuidelines.pdf. 
[Accessed: Nov. 14, 2025].
```

### Thesis/Dissertation
```latex
\bibitem{johnson2023}
S. Johnson, ``Thesis Title,'' Ph.D. dissertation, Dept. Industrial Eng., 
University Name, City, State, 2023.
```

## Contributing

Found a bug or have a suggestion? Contributions are welcome!

### How to Contribute

1. **Report issues** - Open an issue describing the problem
2. **Suggest improvements** - Share ideas for better formatting or usability
3. **Submit fixes** - Fork, fix, and submit a pull request
4. **Share examples** - Contribute example papers using the template

### Contribution Guidelines

- Test changes thoroughly by compiling the template
- Maintain compatibility with standard LaTeX distributions
- Update documentation for any formatting changes
- Follow existing code style and commenting conventions
- Explain the rationale for changes clearly

## License

This template is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

### What This Means

**You are free to:**
- **Share** — Copy and redistribute the template in any medium or format
- **Adapt** — Remix, transform, and build upon the template for any purpose, even commercially

**You must:**
- **Give appropriate credit** — Provide attribution to the original authors
- **Provide a link to the license** — Include a reference to the CC BY 4.0 license
- **Indicate if changes were made** — Note any modifications you've made to the template

**Additional freedoms:**
- No additional restrictions — You cannot apply legal terms that restrict others from doing anything the license permits
- No DRM — You cannot apply technological measures that restrict access

**No warranty:**
- The template is provided "as is" without guarantees
- Authors are not liable for any issues arising from use

See the [LICENSE](LICENSE) file for full details, or visit [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Attribution

If you use this template, please provide attribution as follows:

**In your paper's acknowledgments (optional but appreciated):**
```
This paper was prepared using the IISE Annual Conference LaTeX Template.
```

**In repositories or distributions:**
```
IISE Annual Conference LaTeX Template
Licensed under CC BY 4.0
Original template available at: [your-repository-url]
```

## Acknowledgments

- Template based on official IISE Annual Conference formatting guidelines
- Conference proceedings editors: H. Xiao, H.E. Romeijn, Z. Shen, M. Zhou
- Thanks to the IISE community for feedback and testing
- LaTeX community for excellent documentation and support

## Additional Resources

### Official IISE Resources
- [IISE Official Website](https://www.iise.org)
- [IISE Annual Conference](https://www.iise.org/Annual)
- [IISE Submission Guidelines](https://www.iise.org/Annual) - Always check the latest call for papers

### LaTeX Learning Resources
- [Overleaf: Learn LaTeX in 30 Minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
- [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX) - Comprehensive guide
- [The Not So Short Introduction to LaTeX](https://tobi.oetiker.ch/lshort/lshort.pdf) - Classic tutorial
- [LaTeX Stack Exchange](https://tex.stackexchange.com/) - Q&A community

### IEEE Citation Style
- [IEEE Citation Guidelines (PDF)](https://ieee-dataport.org/IEEECitationGuidelines.pdf)
- [IEEE Editorial Style Manual](https://journals.ieeeauthorcenter.ieee.org/your-role-in-article-production/ieee-editorial-style-manual/)
- [IEEE Reference Guide](https://ieeeauthorcenter.ieee.org/wp-content/uploads/IEEE-Reference-Guide.pdf)

### LaTeX Editors
- [Overleaf](https://www.overleaf.com) - Online collaborative LaTeX editor
- [TeXstudio](https://www.texstudio.org/) - Cross-platform LaTeX editor
- [VS Code + LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) - VS Code extension
- [TeXmaker](https://www.xm1math.net/texmaker/) - Another popular editor

## Version History

**Version 1.0** (November 2025)
- Initial release of IISE Annual Conference template
- Based on 2026 conference formatting guidelines
- Includes all required formatting elements
- Comprehensive documentation and examples

## Contact and Support

### Getting Help

1. **Check this README** - Most questions are answered here
2. **Review the template comments** - Extensive inline documentation
3. **Consult IISE guidelines** - Official call for papers has the final word
4. **LaTeX Stack Exchange** - Great for LaTeX-specific questions
5. **Contact IISE** - For conference-specific questions

### Found a Problem?

If you encounter issues with the template:
- Check the Troubleshooting section above
- Verify you have a complete LaTeX installation
- Ensure you're using the latest version of the template
- Report persistent issues via GitHub Issues (if hosted on GitHub)

### Questions About IISE Submission?

For questions about:
- Submission deadlines
- Review process  
- Presentation formats
- Conference registration

Contact the IISE Annual Conference organizers directly through [www.iise.org](https://www.iise.org).

---

## Ready to Write?

You now have everything you need to create a professional IISE Annual Conference paper! 

**Quick reminder:**
1. Copy the template to a new file
2. Update title, abstract ID, abstract, and keywords
3. Write your paper in the sections
4. Add figures, tables, and references
5. Compile twice with pdflatex
6. Check the pre-submission checklist
7. Submit before the deadline!

**Good luck with your submission! 🎉**

---

*This template is maintained by the community. For the latest version and updates, check the repository.*

*Last updated: November 2025*
