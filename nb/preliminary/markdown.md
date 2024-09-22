# Markdown
\
Within notebooks ait is possible to combine text with computations (images, etc) which make them ideal for learning and experimenting.

When writing a `text` cell, it is possible to format our text using very markdown codes. [Markdown](https://www.markdownguide.org/basic-syntax) is a simple way of formatting text to generate different styles. *Markdown* text will be used throughout all the notebooks you will be using, so if you are interested in learning how a certain style or text format was achieved, all you need to do is to open the text cell and examine what codes were used. On ocassion, when *markdown* is not enough to achieve a desired output, it is combined with some basic html coding.

In this section you will learn some basic markdown formatting. It is not meant to be an exhaustive guide (see guidelines below for more information).

```{caution}
Keep in mind that there are different *flavors* of markdown and some offer more formatting possibilities than others. In this book,all text content whether in Jupyter Notebooks (`.ipynb`) or a markdown files (`.md`) is written in a flavor of markdown called **MyST Markdown**. MyST stands for "Markedly Structured Text". It is a slight variation on a flavor of markdown called "CommonMark" markdown.
```

## Basic text formatting

You can use the following codes to achieve

```{list-table} 
:header-rows: 1
:label: basic text coding

* - Markdown
  - Output
* - \#
  - # Title
* - \##
  - ## Subtitle
* - \###
  - ### Small Title
* - \####
  - #### Smaller title
* - \*italics* or \_italics_
  - *italics* or _italics_
* - \*\*bold** or \_\_italics__
  - **bold** or __bold__
* - \*\*\*bold_italics*** or \_\_\_bold_italics___
  - ***bold_italics*** or ___bold_italics___
```

## Lists

Use the following code will generate a bulletted lists, 

 ```{code}
- item 1    
- item 2   
- item 3
```
or 

 ```{code}
* item 1    
* item 2   
* item 3
```
to output,
- item 1
- item 2
- item 3

for a numbered list use,

 ```{code}
1. item 1    
2. item 2   
3. item 3
```
to output,

1. item 1   
2. item 2
3. item 3

finally, you can generate nested lists that use straigtht up bullets, numbers or any combination of both,

```{code}
1. item 1
   1. sub-item 1
   2. sub-item 2
2. item 2
   - sub-item 1
   - sub-item 2
```
to produce,

1. item 1
   1. sub-item 1
   2. sub-item 2
2. item 2
   - sub-item 1
   - sub-item 2

```{caution}
Pay close attention to spacing when creating nested lists.
```
## Line breaks

Markdown does not generate a line break after pressing {kbd}`enter`,  {kbd}`return` or {kbd}`⌘`. If you type,
```{code}
there are two 
lines here but appear as one
```
they appear as,

there are two lines here
but appear as one

To be able to separate two lines, you can either include at least 3 trailing spaces at the end of a line or insert the character '\\' to jump to a new line.

## Links

You can easily generate a link that connects to some HTML document (like a website). The following,

```{code}
This is a link to the [DiGAR Lab](https://www.digarlab.uw.edu/) home website.
```
will show as,   

This is a link to the [DiGAR Lab](https://www.digarlab.uw.edu/) home website.


## Additional References
* To learn about [Markdown](https://www.markdownguide.org/basic-syntax/) in general.
* To learn about [MyST](https://mystmd.org/) flavor of markdown.


