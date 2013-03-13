Food Journal: WordPress Post Generator
======================================

Food Journal is a Python script that allows users to create an
automated WordPress blog with photos of the food they eat and breif
descriptions of the food.

An example Food Journal WordPress site lives [here][1].

I am also working on an [Android app][2] and a [WXPython Desktop GUI][3].

Installation Instructions
-------------------------

1. Create your own [WordPress blog][4].
2. Enter your meal contents in the `Food Journal.xlsx` file, with the contents
   of the meal separated by semicolons, like so: `Eggs with cheese; Bacon`.
   <em>Make sure to retain the excel file's format, with the rows and column
   format as given.  Feel free to add more rows, but additional columns, or meal
   types are not supported.</em>
3. Update config.ini such that it points to your blog, photos and the Excel 
   file.
4. Put some `.jpg` photos, taken on the day from the Excel file, in the Photo
   directory.  Do not worry about file names, they will be changed automatically 
   upon uploading.
5. Run `$ python WordPressPostGenerator.py`.

How it Works
------------

Food Journal works best in conjunction with [Dropbox Camera Upload][5], 
which automatically uploads photos from your phone to your Dropbox 
folder.  This script checks for new entries in the Excel file, and for 
each date that does not have a post on your blog, it pulls photos from 
the photo directory.  When you give your WordPress password, it autoformats
and uploads the photos and descriptions to your blog, creating one or more
posts (one post per day).

Known Bugs / Future Changes
---------------------------

- Adding new meal types is not supported.
- All photos added must have metadata indicating that it was taken on the 
  day of the post.
- Non-Excel file formats are not supported (Sorry!).
- Incorrect formating of the Excel file will cause errors (Don't forget your
  semicolons!).


[1]: http://dansfoodjournal.wordpress.com
[2]: https://github.com/danrschlosser/FoodJournal-Android/
[3]: https://github.com/danrschlosser/LearningWXPython
[4]: http://wordpress.com/
[5]: https://www.dropbox.com/help/289/en

