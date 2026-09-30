# Debug log

Your notes. One entry per bug you fixed, using the template below.

This file is read as carefully as your code. A correct fix you cannot
explain counts for little; a bug you could not fix but investigated
honestly still counts for something.

Delete the example before you submit.



## Example — delete this

### CC-99 — "The cart total is wrong"

**Reproduced:** Added 2 dosas at Rs. 60 each. The cart showed
Rs. 119.99999 instead of Rs. 130. Happened every time, on any dish with
a price ending in .50.

**Cause:** The total was being added up with plain floating point and
never rounded, so 0.1 + 0.2 style errors showed up on screen. The
rounding helper existed but this one place was not using it.

**Fix:** Ran the total through the existing rounding helper instead of
adding a new one, so every price on screen goes through the same path.

**Checked:** Cart, checkout and the order screen all show Rs. 130 now.
Prices without decimals still show without a trailing .00.

**Time:** about 40 minutes, most of it working out that the cart and the
order screen round in different places.



## CC-0X — "<the complaint, in short>"

**Reproduced:**

**Cause:**

**Fix:**

**Checked:**

**Time:**



## Could not fix

For anything you investigated but did not solve. Say what you tried and
where you got to. This is worth marks — leaving it blank when you got
stuck is not.

### CC-0X — "<the complaint>"

**What I tried:**

**Where I got to:**

**What I would try next:**



## Extra credit

Anything not on the bug log: a problem you found yourself, a test you
wrote, or a fix you are unsure about. Same format, plus one line on how
you noticed it.


-----------------------

### CC-01 : "The search suggestions are behind everything"

**Reproduced:** I searched

**Cause:** Z-index of the parent class of the suggestion box was lower than the categories section

**Fix:** changed the Z-index of .search-wrap from 1 to 50

**Checked:** the suggestion box is now displayed correctly above the categories section

**Time:** 15 minutes

### CC-02 : "Can't read anything in dark mode"

**Reproduced:** Switched to dark mode 

**Cause:** The dish name and prices color was not defined so they were using the default color

**Fix:** Applied the theme-aware --ink color so the dish names and prices automatically use the appropriate color in light and dark mode

**Checked:** the text is now visible in dark mode

**Time:** 10 mins

### CC-03: "The menu is wider than my phone"

**Reproduced:** change the device to smallest mobile screen (320x558) and the menu was overflowing 

**Cause:** Dish-card was not able to shrink below its content's intrinsic width

**Fix:** Added min-width: 0 to allow the dish card to shrink properly 

**Checked:** Verified that the menu now fits on smaller screens

**Time:** 8 mins

### CC-04: "The buttons don't work on my tablet"

**Reproduced:** change the device to ipad mini and the add to card and favorite button was not working

**Cause:** .dish-card::after and .img-wrap::after were overlapping on the buttons 

**Fix:** Added pointer-events: none

**Checked:** Verified that the buttons work properly 

**Time:** 8 mins 


