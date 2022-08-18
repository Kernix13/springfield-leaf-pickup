# springfieldleafpickup

This is a simple JavaScript application to calculate the schedule each year for leaf pickup in Springfield Township, Pennsylvania.

## Reason for the project

I thought it would be a good exercise to write some JavaScript to calculate the schedule.

I started it when I was searching for the 2021 scheule and found two online PDF files for the previous years. I noticed a pattern, had to make some assumptions, then used JavaScript to output the schedule based on the current year.

I contacted the township about a version of this on [CodePen](https://codepen.io/jim-kernicky/pen/PoJqzMd) but they did not get back to me.

## The assumptions

I had to make assumptions because Springfield Township never replied to my email:

1. That the 1st week of leaf pickup is the week of the first Monday in November. But what if November 1st is on a Tuesday? Will the 1st week start on Monday October 31st or the follwoing week on Monday November 7th?
1. That the number of Precints do not increase or decrease - no changes.
1. That the order of precincts do not change.
1. That the two holiday weeks, week 2 and 4, have 1 less precinct that the other weeks, and that remains constant.
1. That the number of weeks do not change, no increase or decrease.

If 1 or more of those assumptions are wrong then this will _NOT_ output the correct schedule. Based on the 2 PDF files I found online and some logic, I think my assumptions are correct.
