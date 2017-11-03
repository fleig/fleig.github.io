# To join PDF files use the following commands

## Example1

```bash
$ qpdf --empty --pages input1.pdf input2.pdf -- output.pdf
```

*--empty* is to create a blank PDF

## Example2

```bash
$ qpdf --empty --pages input1.pdf 1-5 input2.pdf 2-6 -- output.pdf
```

the number after the corresponding PDF, indicates which pages are going to save in the output PDF file..