# File structure basics

You probably will not need to spend much time with this, however, it is important to have some basic understanding about how a computer structures files. This is particularly true the moment you run into the following error or similar,

``` python
    data1 = open(r"c:\courses\archy5_235\termA\data\week1.txt")
```
```
---------------------------------------------------------------------------
FileNotFoundError                         Traceback (most recent call last)
Cell In[9], line 1
----> 1 open(r"c:\courses\archy5_235\termA\data\week1.txt")

File C:\Python\Miniconda3\envs\graffiti_book\Lib\site-packages\IPython\core\interactiveshell.py:324, in _modified_open(file, *args, **kwargs)
    317 if file in {0, 1, 2}:
    318     raise ValueError(
    319         f"IPython won't let you open fd={file} by default "
    320         "as it is likely to crash IPython. If you know what you are doing, "
    321         "you can use builtins' open."
    322     )
--> 324 return io_open(file, *args, **kwargs)

FileNotFoundError: [Errno 2] No such file or directory: 'c:\\courses\\archy5_235\\termA\\data\\week1.txt'
```

You will encounter the above error anytime that you are trying to access a file and the computer cannot find it. There might be several reasons for this:
- the file you are trying to open does not exist
- the filepath is incorrect
- the filename is incorrect
- the file extension is incorrect

## File hierarchy

Every file in your computer is stored somewhere (some location on a drive). To be able to use it (open it, write to it, read it) you need to be able to access it. Typically, files in a drive are stored inside *directories* or *folders* and these can be *nested* i.e. you can have one inside another and so on.

The name of the drive plus the folders in which a file is located create what is called a *Path*. You can think of the path of a file to be similar to an address. The same way that you are in some country (e.g. US), inside a particular region (e.g. WA) within a particular city (e.g. Seattle) and so on, a file's path indicates where the file resides in some drive. Typically, a path looks something like the following,

```c:\courses\archy5_235\termA\data\week1.txt```

In this particular case, the *drive* is a local drive called `c` and the file (most likely, a text file in this case, given the `.txt` ending) resides inside a folder or directory called `data` which in itself is inside `termA`, which in turn is inside `archy5_235` within the `courses` folder or directory. Unless you provide your code with the correct location of the file, your computer will spit out an error similar to the one we saw above.

```{note}
In the previous example, each subfolder or directory is separated by a *special character* which in this case is the *forward slash* '/'. This may be different depending on what operating system you are using (e.g. Windows, MacOS or Linux)
```

The following provides you with information needed to handle well files.

## Display Current Working Directory or Folder

In order to see within a notebook what is your current directory or folder you can use the following *magic* command,

```{code}
%pwd
``` 

which stands for **p**rint **w**orking **d**irectory.


## List Files and Directories or Folders

To list all the files and folders or directories that are in your current directory or folder you can type.

```{code}
%ls
``` 


## Change Directories or Folders

To change to a different folder or directory you need to use the following,
```{code}
%cd path/
``` 

which stands for **c**hange **d**directory. 

You can use a *double dot* '. .' after `cd` to indicate that you want to move to the folder or directory immediately above to your current one.

```{code}
%cd ..
``` 

## Absolute and Relative *filepaths*

There are two different ways to tell the computer where to find a file. 

### Absolute Path
By providing an **absolute** filepath you identifies the location a file **regardless** of where the command referencing that file is at (i.e. regardless of your current working directory). E.g.,

```{code}
%cd c:\courses\archy5_235\termA\data\week1.txt
``` 

### Relative Path

By providing a **relative** filepath you identify the location of a file relative to your current location (i.e. current working directory). Let's consider an example.Imagine you have the following file structure,

```
c:
  dir1
      code1.py
      data1.txt
  dir2
      code2.py
      data2.txt
      data3.txt
```
We are currently in `dir1` running `code1.py` and we want to open `data2.txt`. The relative filepath that we will need to use is the following,
```{code}
`..\dir2\data2.txt`
```
This tells the computer that in order to fetch `data2.txt` file it needs to go up one level, represented by the two dots: '. .' (remember we are in `dir`) then down into `dir2` where it will find `data2.txt`

```{hint}
Are you still confused?
The difference between an absolute and a relative filepath is similar to the difference between providing your address to someone who does not live in your country (~ absolute filepath) and someone that lives in your city, i.e relative to where you live (~ relative filepath)  