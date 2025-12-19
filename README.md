# IISE Annual Conference LaTeX Template

A professional LaTeX template for preparing manuscripts for submission to the Institute of Industrial and Systems Engineers (IISE) Annual Conference. This template is fully compliant with the official IISE Annual Conference formatting guidelines.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## 🚀 Quick Links

- **[Open in Overleaf](https://www.overleaf.com/project/6944ba0bfb0cbf04f1d184d3)** - Start using the template immediately (no installation required)
- **[GitHub Repository](https://github.com/bankh/IISE-Annual-Conference-LaTex-Template)** - Download and customize locally

## Features

- ✅ **Fully compliant** with official IISE Annual Conference formatting guidelines
- ✅ **Blind review support** - Easy toggle between blind and non-blind versions
- ✅ **BibTeX integration** - IEEE style references with automated bibliography
- ✅ **Professional formatting** - All spacing, fonts, and layouts pre-configured
- ✅ **Examples included** - Figures, tables, equations, and citations
- ✅ **Well-documented** - Clear comments throughout the template

## Quick Start

### Option 1: Use Overleaf (Easiest - No Installation Required)

1. Click **[Open in Overleaf](https://www.overleaf.com/project/6944ba0bfb0cbf04f1d184d3)**
2. Make a copy of the project to your Overleaf account
3. Start editing and compile with one click!

### Option 2: Local Installation

#### Prerequisites

You need a LaTeX distribution installed:
- **Windows**: [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)
- **macOS**: [MacTeX](https://www.tug.org/mactex/)
- **Linux**: TeX Live (`sudo apt-get install texlive-full`)

#### Compilation

To compile the document with BibTeX references:

```bash
pdflatex "IISE Annual Conference Template.tex"
bibtex "IISE Annual Conference Template"
pdflatex "IISE Annual Conference Template.tex"
pdflatex "IISE Annual Conference Template.tex"
```

Or use your LaTeX editor's build system (most editors handle this automatically).

## Document Structure

### Page Layout

- **Page Size**: 8.5" × 11" (Letter)
- **Margins**: 1.00" on all sides (top, bottom, left, right)
- **Page Limit**: 6 pages maximum (including title, author data, references, figures, and tables)
- **Spacing**: Single line-spacing with full-justified text
- **Paragraphs**: No indentation; single blank line between paragraphs
- **Headers/Footers**: First page has conference proceedings editors' information; no page numbers

### Title Page Elements

#### Paper Title
- **Font**: 16-point, Times New Roman, bold, centered
- **Case**: Upper and lower case

#### Abstract ID
- **Font**: 12-point, Times New Roman, bold, centered
- **Location**: Below title

#### Author Information
- For **blind review**: Set `\def\blind{1}` - author info will be hidden
- For **final submission**: Set `\def\blind{0}` - author info will be displayed
- **Font**: 10-point, Times New Roman
- **Format**: Names with superscript affiliations, then affiliation details

#### Abstract
- **Heading**: 12-point, Times New Roman, bold, centered
- **Text**: 10-point, Times New Roman, full-justified
- **Length**: Maximum 250 words
- **Spacing**: Single blank line before and after

#### Keywords
- **Heading**: 12-point, Times New Roman, bold, left-justified (not numbered)
- **Text**: 10-point, Times New Roman
- **Quantity**: 3-5 keywords
- **Note**: This section does not have a section number

### Text Sections and Headings

#### Main Section Headings
- **Format**: Numbered, 12-point, Times New Roman, bold, left-justified
- **Spacing**: One blank line above only

#### Subsection Headings
- **Format**: Numbered, 10-point, Times New Roman, bold, left-justified
- **Spacing**: One blank line between subsections

#### Sub-subsection Headings
- **Format**: Numbered, 10-point, Times New Roman, bold, left-justified

#### Regular Text
- **Font**: 10-point, Times New Roman, full-justified
- **Spacing**: Single line between paragraphs

### Bullets

The template supports three levels of bullets:
- **First level**: Bullet point (•)
  - **Second level**: Open bullet (○)
    - **Third level**: En dash (–)

### Figures, Tables, and Captions

#### Tables
- **Placement**: In main text, close to point of introduction
- **Caption Position**: Above the table
- **Caption Font**: 10-point, Times New Roman
- **Caption Alignment**: Centered (single line) or full-justified (multiple lines)
- **Spacing**: One blank line above and below the caption
- **Numbering**: Independent from figures (Table 1, Table 2, etc.)

#### Figures
- **Placement**: In main text, close to point of introduction
- **Caption Position**: Below the figure
- **Caption Font**: 10-point, Times New Roman
- **Caption Alignment**: Centered (single line) or full-justified (multiple lines)
- **Spacing**: One blank line above and below the caption
- **Numbering**: Independent from tables (Figure 1, Figure 2, etc.)
- **Note**: Text should not wrap around figures

#### Figure and Table Guidelines
- Include both in main text as close to their introduction as possible
- Figure and table numbering should be independent
- Labels within figures should be legible
- Supported formats: PDF, PNG, JPG

### Equations

- **Alignment**: Centered
- **Numbering**: Sequential, in order of appearance
- **Number Position**: In parentheses, flush to right margin
- **Spacing**: One blank line before and after every equation
- **Preparation**: Use equation editor (not screenshots)
- **Citation**: Refer to equations as "Equation (1)" in text

Example usage:
```latex
\begin{equation}
t_{align} = \frac{9\lambda\eta\rho_a}{2\pi kr^2 \Phi} \ln\left(\frac{\tan(kx_0)}{\tan(kx_f)}\right)
\label{eq:example}
\end{equation}
```

### Acknowledgements

- **Section Name**: "Acknowledgements" (no section number)
- **Location**: Immediately before "References and Citations" section
- **Content**: Funding support and/or any other assistance
- **Blind Review**: Automatically anonymized when `\blind{1}`

### References and Citations

#### Citation Style
- **Format**: IEEE style
- **In-text**: Square brackets with numbers [1]
- **Numbering**: Sequential by order of occurrence (not alphabetical)
- **Multiple citations**: 
  - Two references: [2, 3]
  - Consecutive range: [2-4]

#### Using BibTeX (Recommended)

1. Add references to `references.bib` file:
```bibtex
@article{yodo2016,
  author = {Yodo, N. and Wang, P.},
  title = {Resilience Allocation for Early Stage Design of Complex Engineered Systems},
  journal = {Journal of Mechanical Design},
  volume = {138},
  number = {9},
  pages = {091402 (10 pages)},
  month = {July},
  year = {2016},
  doi = {10.1115/1.4033990}
}
```

2. Cite in text:
```latex
\cite{yodo2016}           % Single citation: [1]
\cite{ref1,ref2}          % Multiple: [1, 2]
\cite{ref1,ref2,ref3}     % Range: [1-3]
```

3. Compile with BibTeX (as shown in Quick Start)

#### Reference Types Supported
- Journal articles
- Conference proceedings
- Books
- Online sources
- Technical reports

## Blind Review Mode

The template includes built-in support for blind review:

### Enable Blind Review (for submission)
```latex
\def\blind{1}
```

This will:
- Hide author names and affiliations
- Display: "Author information is purposely removed for blind review"
- Anonymize acknowledgements section

### Disable Blind Review (for camera-ready)
```latex
\def\blind{0}
```

This will:
- Show full author information
- Display complete acknowledgements
- Include all identifying information

## File Structure

```
IISE-Annual-Conference-LaTeX-Template/
├── IISE Annual Conference Template.tex  # Main LaTeX file
├── references.bib                        # BibTeX references database
├── README.md                             # This file
├── .gitignore                            # Git ignore rules
└── example-figure.pdf                    # (Your figures go here)
```

## Customization

### Updating Author Information

Edit the non-blind section in the template (around line 106):

```latex
\if0\blind
% NON-BLIND VERSION: Show title, Abstract ID, and author information
\begin{center}
{\fontsize{16}{19}\bfseries\selectfont 
Your Paper Title Here}

\vspace{10pt}

{\fontsize{12}{14}\bfseries\selectfont Abstract ID: 1234}

\vspace{10pt}

% Author information (shown in non-blind version)
{\fontsize{10}{12}\selectfont
First Author$^{a}$ and Second Author$^{b}$ \\
\vspace{5pt}
$^{a}$Department Name, University Name, City, Country \\
$^{b}$Department Name, University Name, City, Country}
\end{center}
\fi
```

### Adding Figures

Replace the placeholder figure with your own:

```latex
\begin{figure}[h!]
\centering
\includegraphics[width=0.6\textwidth]{your-figure.pdf}
\caption{Your figure caption here}
\label{fig:yourfigure}
\end{figure}
```

### Adding References

Add new entries to `references.bib` following IEEE format, then cite with `\cite{key}`.

## Tips and Best Practices

1. **Start early** - LaTeX formatting takes time to perfect
2. **Compile frequently** - Catch errors early
3. **Use version control** - Git is recommended (`.gitignore` included)
4. **Check page limit** - Maximum 6 pages including everything
5. **Proofread carefully** - Especially after switching blind mode on/off
6. **Test compilation** - Always do a full compile (pdflatex → bibtex → pdflatex → pdflatex)
7. **Avoid manual formatting** - Let LaTeX handle spacing and alignment
8. **Use labels** - Reference figures, tables, and equations with `\ref{}`

## Common Issues and Solutions

### Issue: References not appearing
**Solution**: Make sure to run BibTeX and cite references in text with `\cite{}`

### Issue: Figures in wrong location
**Solution**: Use `[h!]` or `[H]` placement specifier, or let LaTeX decide

### Issue: Bibliography has gaps between items
**Solution**: Already fixed in template with `etoolbox` package

### Issue: PDF not updating
**Solution**: Delete auxiliary files (`.aux`, `.bbl`, `.blg`) and recompile

## Requirements

### Required LaTeX Packages
- `geometry` - Page layout
- `times` - Times New Roman font
- `graphicx` - Figure support
- `amsmath` - Equation support
- `cite` - IEEE style citations
- `url` - URL formatting in references
- `fancyhdr` - Custom headers
- `titlesec` - Section formatting
- `caption` - Caption formatting
- `parskip` - Paragraph spacing
- `enumitem` - Bullet list formatting
- `etoolbox` - Environment patching

All packages are included in standard LaTeX distributions.

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test compilation thoroughly
5. Submit a pull request with clear description

## Version History

- **v1.0** (2025-11-14)
  - Initial release
  - Blind review support
  - BibTeX integration
  - Full IISE compliance

## License

This template is released under [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material

Under the following terms:
- **Attribution** — You must give appropriate credit

## Contact

**Author**: Hasan Sinan Bank  
**Email**: sinan.bank@colostate.edu  
**Repository**: https://github.com/bankh/IISE-Annual-Conference-LaTex-Template

## Acknowledgements

This template is based on the official IISE Annual Conference formatting guidelines. Special thanks to the IISE community for feedback and contributions.

## Support

If you encounter issues or have questions:
1. Check this README thoroughly
2. Review the comments in the `.tex` file
3. Open an issue on GitHub
4. Contact the author via email

---

**Happy writing! 📝**
