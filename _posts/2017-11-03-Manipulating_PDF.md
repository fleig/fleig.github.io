---
layout: post
title: Manipulating PFD via command-line!
---

## To join PDF files use the following commands

#### Example1

```bash
$ qpdf --empty --pages input1.pdf input2.pdf -- output.pdf
```

*--empty* is to create a blank PDF

#### Example2

```bash
$ qpdf --empty --pages input1.pdf 1-5 input2.pdf 2-6 -- output.pdf
```

the number after the corresponding PDF, indicates which pages are going to save in the output PDF file...

---

## To reduce PDF filesize use the following commands

#### Example1

```bash
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
```

-dPDFSETTINGS=

| Parameter | Quality |   Size  | Size(MB) |
|:---------:|:-------:|:-------:|:--------:|
|  /screen  |  Lower  | Smaller |    4.5   |
|   /ebook  |   Low   |  Small  |    5.8   |
|  /printer |   Good  |  Medium |    8.4   |
| /prepress |  Better |  Medium |    9.7   |
|      -    |    -    |    -    |    -     |
|  Original |   Best  |   Big   |   69.8   |