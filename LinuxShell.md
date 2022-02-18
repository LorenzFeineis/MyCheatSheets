## `pdftk`

`apt-get install pdftk`

example: \

`pdftk A=input1.pdf
   B=input2.pdf
   cat A1right A2-end Beven
   output output.pdf`

Concatenates all pages of input1.pdf, where the first page is rotated to the left
and all even pages of input2.pdf.

## `gs`

`gs -sDEVICE=pdfwrite \
   -dPDFFitPage \
   -r300x300 \
   -g<w>x<h> \
   -o output.pdf \
   input.pdf`

Fits all pages in a pdf to the page size w x h.

## Helpful commands

* `cat`: Concatenates files and prints on the standard output
* `grep`: print lines that match patterns

## System information:

* ``
