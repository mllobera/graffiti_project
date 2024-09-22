# Documentation    
\
Documentating code is a **very** important part of coding. Through documentation you can provide essential information to the user about how to use your code properly. As importantly, it provides you (the developer of code) much needed information about your own code which is particulaly important after time has passed since you last used or looked at it.

Documenting code is a bit of a fine art. If you are too brief, you might not be able to make heads or tails of your own code. If too long or verbose, the text gets in the way, and you will not be able to read well how your program flows or it is structured.

The following it is meant to give you the very bare essentials and to make you aware of the importance of documentation in case you were to carry on with your coding beyond this class.

### Inline comments
These tend to be short comments, primarily meant for you, the developer, that summarize
what a block of code does.

``` python
    # initialize graphic variables
    ...

    # any user input?
    ...
```
### Docstrings
These are the comments that we include when writing functions, modules and packages. They are written primarily for the user, to provide them information about the purpose of a function or module. They are enclosed by triple single quotes `'''`. . .`'''`. They can be very brief, i.e. just a single one-liner,
``` python
    def stats(<parameters>):
        '''calculates descriptive statistics of a graffiti''' 
```
or much more elaborate,
``` python
    def find_writer_scope(table):
        '''Calculates centroid and radius of each distinct writer
        
        Parameters:
            - table: csv file
                table with location and name of each writer
        Returns:
            - centroid: float
                centroid of all writer's locations
            - radius: float
                radius for the circle enclosing all
        '''
                        .
                        .
                        .
```
```{note}
There are many different docstring 'styles' of [documenting](http://daouzli.com/blog/docstring.html). 
```

## Additional References
- To learn more about why it is [important documentation](https://realpython.com/documenting-python-code/)
- Here is a good [guide](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/) compiled from expert programmers. 