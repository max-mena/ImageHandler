# ImageHandler

A Python desktop application that loads image metadata from `.bdjson` files and renders the images in a graphical interface.

## What it does

1. Opens a file picker filtered to `.bdjson` files
2. Parses the JSON array of `{ url, nombre }` objects
3. Downloads each image via HTTP
4. Displays all images horizontally at 100×100 px with their names centered below

## Tech Stack

- Python 3
- `requests` — HTTP image fetching
- `Pillow` — image processing
- `tkinter` — GUI (standard library)

## Setup

```bash
# Create and activate virtual environment
pyenv exec python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

Click **"Abrir base de datos"** and select a `.bdjson` file.

## Input Format

```json
[
  { "url": "https://example.com/image1.jpg", "nombre": "Image 1" },
  { "url": "https://example.com/image2.jpg", "nombre": "Image 2" }
]
```

An `example.bdjson` file is included in the repository.
