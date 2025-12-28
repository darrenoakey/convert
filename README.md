![](banner.jpg)

# convert

A self-healing file format conversion tool that automatically figures out how to convert between any file formats.

## Purpose

`convert` is a command-line tool that converts files between different formats. Point it at any file and tell it what format you want - it handles the rest automatically.

The tool:
- Automatically selects the best conversion method for your file types
- Creates and caches converters for future use
- Self-heals when conversions fail, automatically fixing issues and retrying

## Installation

Requires Python 3.8+ and the following dependencies:

```bash
pip install pydantic colorama claude-agent-sdk
```

Make the script executable:

```bash
chmod +x convert
```

## Usage

```bash
convert <source_file> <target_file>
```

Or use shorthand notation with just the target extension:

```bash
convert <source_file> <target_extension>
```

## Examples

Convert an image from PNG to JPEG:

```bash
convert photo.png photo.jpg
```

Using shorthand extension notation:

```bash
convert photo.png jpg
convert photo.png .jpg
```

Convert a video file:

```bash
convert video.mov video.mp4
```

Convert an audio file:

```bash
convert song.wav mp3
```

Convert a document:

```bash
convert document.docx pdf
```

## Notes

- First-time conversions for a format pair may take longer as the tool sets up the converter
- Subsequent conversions of the same format pair use the cached converter
- Converter scripts are stored in the `convert_data` directory alongside the tool