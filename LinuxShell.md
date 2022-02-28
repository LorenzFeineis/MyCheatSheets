## pdf handling

Concatenate all pages of input1.pdf, where the first page is rotated to the left and all even pages of input2.pdf: \
`pdftk A=input1.pdf
   B=input2.pdf
   cat A1right A2-end Beven
   output output.pdf`

Fit all pages in a pdf to the page size w x h: \
`gs -sDEVICE=pdfwrite \
   -dPDFFitPage \
   -r300x300 \
   -g<w>x<h> \
   -o output.pdf \
   input.pdf`

Converting markdown or text files to pdf: \
`pandoc file.md -o file.pdf`

Convert an concatenate formats jpeg, jpg, png and other into one pdf file: \
`convert -compress <format> <input> <output.pdf>`

## Helpful commands

* `ls | wc -l`: count all entrees in the current workind directory
* `cat`: Concatenates files and prints on the standard output
* `grep`: print lines that match patterns \
   e.g. `grep TODO *` - prints all files and lines that contain "TODO"

## System information:

* ``

## Running programs in parallel with `xargs`
Running each line in batch.bat as a bash command, use 4 kernels at the same time: \
`xargs -a batch.bat -d'\n' -n 1 -P4 --replace --verbose bash -c {}`

Apply command to output of `ls` or any other list of inputs: \
`ls | xargs -d\'n' -n 1 -P4 <command>`
