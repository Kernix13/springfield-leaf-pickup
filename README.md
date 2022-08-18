# springfieldleafpickup

This is a simple JavaScript application to calculate the schedule each year for leaf pickup in Springfield Township, Pennsylvania.

## Reason for the project

I thought it would be a good exercise to write some JavaScript to calculate the schedule.

I started it when I was searching for the 2021 scheule and found two online PDF files for the previous years. I noticed a pattern, had to make some assumptions, then used JavaScript to output the schedule based on the current year.

I contacted the township about a version of this on [CodePen](https://codepen.io/jim-kernicky/pen/PoJqzMd) but they did not get back to me.

## The assumptions

I had to make assumptions because Springfield Township never replied to my email:

1. The 1st week of leaf pickup is the week of the first Monday in November. But what if November 1st is on a Tuesday? Will the 1st week start on Monday October 31st or the follwoing week on Monday November 7th?
1. The number of precints do not increase or decrease.
1. The order that precincts follow in the schedule is constant and does not change.
1. The number of precincts per week does not change.
1. The two holiday weeks (week 2 and 4) only have 3 precinct while the other weeks have 4.
1. The number of weeks of leaf pickup (currently 6) does not change.

If 1 or more of those assumptions are wrong then this will _NOT_ output the correct schedule. Based on the 2 PDF files I found online and some logic, I think my assumptions are correct.

## Refactor

Take a look at the [commit](https://github.com/Kernix13/springfield-leaf-pickup/commit/8bfde6dc9e4ccb542d48f3f14f69b4e7795d3fc5) before my refactoring to see the before and after of this project.

**NOTE**: This was a project early in my JavaScript studies. Until I refactored it, it did not have a single function - and it worked! How ridiculous is that? I believe the original code is known as _imperative code_.

1. Changed main `for` loop to a `map()` function.
1. Changed 18 `let` keywords to `const`
1. Converted the "check the current year and update the startYr variable" code block into the function `yearCheck(yr)`
1. Created function `findFirstMonday(day)` and added the switch statement inside
1. Created the function `currYrSched(num)` and added inside the code that gets the current years schedule.
1. Created the function `outputSchedule(arr)` and added the code that outputs the `<li>` items based on the weekely indices.
1. Removed all `console.log` statements.
