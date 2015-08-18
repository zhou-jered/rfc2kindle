This project is to convert RFC and I-D into well formatted mobi files so that it can read on Kindle or other eReader.

If you had tried to read RFC from kindle, you knew what the problem is; figures are not showing correctly, there's no jumping from TOC, texts are flowing crazy etc.

This program will create Table of Contents just like other professional publish does. Figures and tables inside the text will be detect and convert into image. Page's header and footer are removed. Chapters will be correctly detected. The goal is make the output has the same feeling as on the printer.

This utility will download rfc text file from ietf.org first, then convert it
into html and images, eventually it will call the kindlegen program to convert html into mobi. Images are created by PIL(Python Image library), as GIF format.

# Download pre-converted mobi files from Google Storage Server #
I have converted all RFCs into mobi format. You can download the RFC you want from
http://commondatastorage.googleapis.com/rhuang/rfcXXXX.mobi  (replace with your number).

# Create by yourself #
1. Download from [link](http://code.google.com/p/rfc2kindle/downloads/list). <br />
2. Download kindlegen from http://www.amazon.com/gp/feature.html?ie=UTF8&docId=1000234621 <br />
3. Make sure you have Python Image Library installed. <br />
4. Run the program with. <br />
```

Usage: rfc2mobi [options] <rfcXXXX|url>

A program to convert RFC or I-D to mobi formatted eBooks.
Options:
  -k ..., --kindlegen=...  The kindlegen program to use. By default, it's "./kindlegen"
  -h, --help

If you want to convert a RFC, just give the RFC name as command line option.
For I-D, specific the link where it can download.
For example
     $ ./rfc2mobi RFC3220
     $ ./rfc2mobi http://www.rfc-editor.org/internet-drafts/draft-zhu-mobileme-doc-05.txt
```