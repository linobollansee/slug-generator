# Slug Generator

A minimal, single-file web tool for generating URL-friendly slugs from text input.

## Features

- **Real-time conversion**: Generates slugs as you type
- **Minimal footprint**: Pure HTML/JavaScript in a single file (< 200 bytes)
- **Smart formatting**:
  - Converts to lowercase
  - Removes diacritics/accents (e.g., é → e)
  - Replaces non-alphanumeric characters with hyphens
  - Trims leading/trailing hyphens
- **No dependencies**: Works instantly in any modern browser

## Usage

Simply open `index.html` in a web browser. Type any text into the input field and the slug will appear below in real-time.

### Example

Input: `Hello World! This is a Test 123`  
Output: `hello-world-this-is-a-test-123`

## Technical Details

The slug generation uses:
- `toLowerCase()` - Convert to lowercase
- `normalize('NFKD')` - Decompose Unicode characters
- Character class replacement to remove diacritics and standardize separators
- Regex cleanup to remove leading/trailing hyphens

## License

Public domain / MIT - Use freely for any purpose.
