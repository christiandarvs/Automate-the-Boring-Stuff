## Reading and Writing Files

## 2 properties of files:
- filename
- path (location of a file on the computer)

## Join Paths - ``/``
- This is helpful for modifying a
``Path object`` after you’ve already created it with the ``Path()`` function.
- The **first two values must be a Path object** when joining them.
- Python evaluates the / operator from **left to right** and evaluates to a Path object, so **either** the first or
second leftmost value must be a Path object for the entire expression to evaluate to a Path object.

## Absolute vs Relative Paths
- **absolute path**, which always begins with the root folder
- **relative path**, which is relative to the program’s current working directory

![](./images/image.png)

## Create new folders - ``os.makedirs()``

- Note that ``mkdir()`` can only make one directory at a time; it won’t make several subdirectories at once like ``os.makedirs()``.