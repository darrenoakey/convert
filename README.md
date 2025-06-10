# Convert Tool

![Banner Image](banner.jpg)

## Purpose

The Convert Tool is a command-line utility designed to convert files from one format to another. It intelligently determines the best method for conversion and attempts to automate the process.

## Usage

To use the Convert Tool, provide the source file and the desired target file as command-line arguments.

```bash
convert <source_file> <target_file>
```

## Examples

1.  Convert a `.png` image to a `.jpg` image:

    ```bash
    convert image.png image.jpg
    ```

2.  Convert a `.txt` file to a `.pdf` file:

    ```bash
    convert document.txt document.pdf
    ```

## Installation

1.  Ensure you have Python 3 installed.
2.  Save the `convert` script to a directory on your system.
3.  Make the script executable:

    ```bash
    chmod +x convert
    ```
4.  Place your OpenAI API key in `~/.openai/openai_api_key.txt`.
5.  (Optional) Add the directory to your `PATH` environment variable for easy access from any terminal location.

### Dependencies

The script relies on the `openai` Python package. It will attempt to install other command-line tools as needed, but it's recommended to have common conversion tools (like `imagemagick`) pre-installed for optimal performance.

Install the OpenAI package using pip:

```bash
pip install openai
```
