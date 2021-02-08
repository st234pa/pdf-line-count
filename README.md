# pdf-line-count

## Count the number of lines of text in a PDF file.

### How to Use

Click [this link](st234pa.github.io/pdf-line-count/) and choose a file from your computer.

### How it Works
PDFs are basically images, so this application parses the PDF and then iterates through each row of pixels and counts the rows such that there are at least two pixels with differing colors and the previous row (if it exists) is single-colored.
For this reason, the input must be a PDF with only text that reads horizontally, a solid color background, and at least one pixel of space between lines.
### Please Note
I threw this together as a simple prototype, so the algorithm is not very robust,
the set of valid inputs is quite limited,
and the user interface is extremely bare bones.
Expanding the set of valid inputs (PDFs with images, multi-colored backgrounds, etc.)
requires a much more complex solution, probably using computer vision.
