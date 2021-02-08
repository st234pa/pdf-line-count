# pdf-line-count

## Count the number of lines of text in a PDF file.

### How to Use

Click [this link](st234pa.github.io/pdf-line-count/) and choose a file from your computer.

### How it Works
PDFs are basically images, so this application uses [PDF.js](https://mozilla.github.io/pdf.js/) to parse the input and then counts the number of rows of pixels that satisfy the following conditions:
- there are at least two pixels in the row that different colors
- if there exists a row above it, that row is single-colored
For this reason, the input must be a PDF with only text that reads horizontally, a solid color background, and at least one pixel of space between lines.
### Please Note
I threw this together as a simple prototype, so the algorithm is not very robust,
the set of valid inputs is quite limited,
and the user interface is extremely bare bones.
Expanding the set of valid inputs (PDFs with images, multi-colored backgrounds, etc.)
requires a much more complex solution, probably using computer vision.
