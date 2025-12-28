![](banner.jpg)

# convert

A self-healing file converter that automatically figures out how to convert between any file formats.

## Purpose

`convert` is a command-line tool that converts files between different formats without requiring you to know which tools or commands to use. Point it at a source file and tell it what format you want, and it handles the rest.

The tool learns as it goes - once it successfully converts between two formats, it remembers how to do it for next time.

## Installation

### Prerequisites

- Python 3.8 or later
- An OpenAI API key stored in your system keyring

### Setup

1. Store your OpenAI API key in the system keyring:
   ```bash
   keyring set openai api-key sk-your-api-key-here
   ```

2. Install Python dependencies:
   ```bash
   pip install openai pydantic colorama keyring
   ```

3. Make the script executable and place it in your PATH:
   ```bash
   chmod +x convert
   ```

## Usage

```bash
convert <source_file> <target_file>
```

The target can be either a full filename or just an extension:

```bash
# Full filename
convert photo.heic photo.jpg

# Just the extension (creates photo.jpg in same directory)
convert photo.heic jpg
convert photo.heic .jpg
```

## Examples

### Image Conversion

```bash
# Convert HEIC to JPEG
convert vacation.heic vacation.jpg

# Convert PNG to WebP
convert logo.png webp

# Convert RAW to JPEG
convert photo.CR2 photo.jpg
```

### Document Conversion

```bash
# Convert Markdown to PDF
convert report.md report.pdf

# Convert DOCX to PDF
convert document.docx pdf
```

### Audio/Video Conversion

```bash
# Convert WAV to MP3
convert recording.wav recording.mp3

# Convert MOV to MP4
convert video.mov mp4

# Convert FLAC to AAC
convert song.flac song.aac
```

### Other Formats

```bash
# Convert SVG to PNG
convert icon.svg icon.png

# Convert CSV to JSON
convert data.csv data.json
```