# UAntwerpen Thesis Typst Template

A Typst conversion of the official UAntwerpen Bachelor/Master thesis LaTeX template.

> **⚠️ Disclaimer:** This is a vibecoded template based on the official UAntwerpen LaTeX thesis template. While functional, there may be some issues or inconsistencies. Feel free to open a PR if you find any problems or improvements!
>
> Also this template was primarily used and tested by students of Digital Business Engineering (faculty `be`). Other faculties should also be supported, but have not been extensively tested.

## Quick Start

1. Rename `example.typ` to `main.typ`
1. Edit `main.typ` with your thesis content
2. Update metadata (title, author, supervisors, etc.)
3. Compile: `typst compile main.typ` or `typst watch main.typ`

## Configuration

Configure the template at the beginning of your document:

```typst
#show: uantwerpen-thesis.with(
  faculty: "ti",
  title: [Your Title],
  author: [Your Name],
  degree: [Master of Engineering\: Electronics and ICT],
  doc-type: [Master's Thesis],
  academic-year: [2024 - 2025],
  supervisors: (([prof. dr. Name], [UAntwerpen]),),
  logo-path: "logos/logo-uantwerpen-ti-en-rgb-pos.pdf",
)
```

## Faculty Codes

`ua` - University (general), `be` - Business/Economics, `fbd` - Pharmaceutical/Biomedical/Veterinary, `ggw` - Medicine/Health, `lw` - Arts, `ow` - Design Sciences, `re` - Law, `sw` - Social Sciences, `ti` - Applied Engineering, `we` - Science, `iob` - Development Policy

Update both `faculty:` and `logo-path:` to match your faculty.

## Key Features

**Inset boxes:**
```typst
#inset-text-ti[Important text]
#inset-quote-ti[Quote or statement]
```

**Appendices:**
```typst
#set heading(numbering: "A.1", supplement: [Appendix])
#counter(heading).update(0)
= First Appendix
```

**Bibliography:**
```typst
#bibliography("references.bib")
```

...

## License

Based on the original LaTeX template by Walter Daems (LaTeX Project Public License v1.3+).
