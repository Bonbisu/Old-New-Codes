# Troubleshooting

## First Sight

While I code this program, I have an issue with a `switch-case` nested on a `for-loop`.At first time running the loop, it takes right the _user input_, after that, every loop pass _"jumps"_ one position going to 3, then 5, and so on...

## Solution

That issue apparently was caused by some _"feature"_ on `C Language` that turns a little hard to work with strings, even catch them from standard input.
The problem was solved giving a space before the _scanf's_ placeholder, I read in some place that occurs beacause `scanf` put a line breaker while catches an input.

## Motivation

I turn back to revisit this code while studying JavaScript loops. The subject was how loops actually works, and in a exercise about "Transform this `while (true) { .. }` loop into a `for (a = 5; a < 10; a++) { .. }`" the solution was:

```js
a = 5; // initialization clause

while (true) {
    /* In order to stop, has needed to negates the conditional 
    !(a < 10) = (a >= 10) | Remember Cachucho and De Morgan */
    if (a >= 10) { 
        break;
    }
}
```

I notice that we uses a `break` statement, and come to try remove all _breaks_ from  the `switch-case` and unfortunatelly doesn't work.

**Pending Updates:** 
- Read an csv file with the correct answers before start assert.
