# pdf-line-count

## Count the number of lines of text in a PDF file.

### How to Use

Click [this link](https://st234pa.github.io/pdf-line-count/), choose a file from your computer, and then click the "Count Lines" button.

### How it Works
PDFs are basically images, so this application uses [PDF.js](https://mozilla.github.io/pdf.js/) to parse the input and then counts the number of rows of pixels that satisfy the following conditions:
- there are at least two pixels in the row that different colors
- if there exists a row right above it, that row is single-colored

For this reason, the input must be a text-only PDF with a solid color background, and at least one pixel of space between lines. White space is not included in the line count and there are some edge cases for which this app will output inaccurate results.
### Please Note
I threw this together as a simple prototype, so the algorithm is not very robust,
the set of valid inputs is quite limited,
and the user interface is extremely bare bones.
Expanding the set of valid inputs (PDFs with images, multi-colored backgrounds, etc.) and catching some contrived edge cases (for instance, a line of all lowercase i's or all ?'s would be counted as two lines instead of one)
would require a much more complex solution, probably using computer vision.

[PDF.js](https://mozilla.github.io/pdf.js/), the only library I used to build this application, is an open source project that is led by the Mozilla Foundation. Everything else is in HTML and vanilla Javascript. 
