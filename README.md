# create-pdf

This is a `pandoc` container for facilitating creation of PDF from sources including

- Markdown
- HTML
- Latex

## Usage

For `--help` run:

```bash
docker run --platform=linux/amd64 ghcr.io/igwejk/create-pdf:latest --help
```

### Generate `PDF` output from `Markdown`

```bash
export pdf_output=/path/to/file/output.pdf
export markdown_input=/path/to/file/input.md
docker run --platform=linux/amd64 ghcr.io/igwejk/create-pdf:latest    \
    --verbose                                                         \
    --pdf-engine=weasyprint                                           \
    --from=markdown+emoji --to=html5                                  \
    --output="${pdf_output}                                           \
    "${markdown_input}"
```
