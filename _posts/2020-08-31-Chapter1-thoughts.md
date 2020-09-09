# Chapter 1 - thoughts and reflections

I finally managed to get through chapter 1 and the labs.  It was a challenge using Gradient as one of the labs continued to get an error.

```python
from fastai.text.all import *

dls = TextDataLoaders.from_folder(untar_data(URLs.IMDB), valid='test')
learn = text_classifier_learner(dls, AWD_LSTM, drop_mult=0.5, metrics=accuracy)
learn.fine_tune(4, 1e-2)
```

I manged to find the solution on the forums, which was to remove the offending directory in a terminal like this:  rm -rf imdb_tok

I also found out that these videos (Lessons 1-8) were part of class given back in March and some of the notes are found on the [forums.](https://forums.fast.ai/t/official-part-1-2020-updates-and-resources-thread/63376/9)

I'm going to go with Paperspace, but I wanted to resolve that error I continued to have above.
It looks like it was the unofficial recommendation based on this forum post by Jeremy back in [March 2020](https://forums.fast.ai/t/official-part-1-2020-updates-and-resources-thread/63376/8)

I did look at Google Colab, and although its easy to link through the guides, something tells me that its better with Gradient being that its a full jupyter environment.
And it tends to be a lot slower than paperspace as I kept running the TextDataLoaders and comparing to the run from Gradient. (now that I have it working)
Note:  All the labs in 01_intro.ipynb worked in Gradient, and WAS working in Google colab.  Then Google colab starting having issues and that sealed it for me.

There is a credit as mentioned here:
```C#
Promotional credit
Paperspace provides $15 of free Gradient credit for using paid instances. 
This code is to be used for Fast.ai students only. 
In your console, click on Billing and enter the promo code at the bottom right. 
The promo code for this course is: FASTAIGR20. 
Note: the code is valid until Dec 31st, 2020
```

In the beginning of Lesson 2, around 38:25 there was a comment made by Jeremy saying that the lessons (1-8) are not meant to cover the entire course.
In the previous courses, there were 14 lessons, and he stated that to get through the book might be 3 courses.

I would imagine that these courses would be forthcoming, but if you wanted to forge ahead, the book is a good reference guide.

I believe I found my strategy.
  1.  Watch the video following along in the printed book version, making notes and annotations best I can
  2.  Read the chapter
  3.  Answer the Questions
  4.  Do the Lab
  5.  Write up for the day
  6.  [Practical Data Ethics course](https://ethics.fast.ai/) (something else to wind down the day)
  
  (or maybe switch between 3/4)
  
  I did quite a bit of work today, and wanted to continue, but if I keep going at this rate, I would finish all the videos before my study group begins!
  That's a goal I should have had last MONTH!
  
  
