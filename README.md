# FujiNet Documentation

User documentation for [FujiNet](https://fujinet.online) — the Wi-Fi network adapter for vintage computers.

Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and deployed automatically to GitHub Pages on every merge to `main`.

## Live site

**https://fujinetwifi.github.io/fujinet-mkdocs/**

## Local development

```bash
pip install -r requirements.txt
mkdocs serve          # live-reload dev server — PDF generation disabled (fast)
```

Open `http://127.0.0.1:8000` in your browser.

### Generating the PDF locally

PDF generation uses [mkdocs-with-pdf](https://github.com/orzih/mkdocs-with-pdf) via WeasyPrint and requires Cairo/Pango system libraries. Enable it by setting `ENABLE_PDF_EXPORT=1`:

```bash
# Linux
sudo apt-get install libpango-1.0-0 libpangoft2-1.0-0 libpangocairo-1.0-0 libgdk-pixbuf-2.0-0 libcairo2

ENABLE_PDF_EXPORT=1 mkdocs build
# Output: site/pdf/fujinet-documentation.pdf
```

> **Note:** PDF generation is known to work on Python 3.10–3.12. Python 3.13+ may have WeasyPrint compatibility issues. The CI pipeline always builds with PDF enabled using Python 3.12.

## Contributing

See [docs/contributing/index.md](docs/contributing/index.md) for the full contribution guide.

Quick edits: use the **Edit** pencil icon on any page of the live site to propose changes directly on GitHub.

## License

Documentation text: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
