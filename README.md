# CoverageBook Tech Test Exercise

## Grade Point Average (GPA) 'Converter'

``` 
STEP ONE - Read through Instructions 
```
``` 
STEP TWO - See failing output by running...

`ruby gpa-test.rb`

Why are tests failing? 
- Just hard-coded 0 in gpa method & '' in announcement method
- No method there to iterate through and calculate required gpa
- Need to create a method to calculate a gpa from given test results
```

## Andy Croll's instructions...


Hi there,

We’d like you complete a short (30-60min) exercise in Ruby. The deadline for this test is (next) Sunday 20th November, we’re hoping to run interviews the following week (or two).

I’ve attached a template file for you to use. The instructions follow... 
If you have any questions or I’ve been unclear please get in touch!

Good luck, don’t stress out.

CoverageBook Technical Exercise
###############################

GPA is grade point average, a way of turning multiple letter grades into a single score between -1 and 4.

https://www.edglossary.org/grade-point-average/

Here are the grades and their respective scores.

A = 4 points
A- = 3.7 points
B+ = 3.3 points
B = 3 points
B- = 2.7 points
C+ = 2.3 points
C = 2 points
C- = 1.7 points
D+ = 1.3 points
D = 1 point
D- = 0.7 points
E+ = 0.5 points
E = 0.2 points
E- = 0.1 points
F = 0 points
U = -1 points

Run the tests by using:

```shell
ruby gpa-test.ruby
```

You'll see a bunch of failing output.

```
(I RAN TESTS TO SEE FAILING OUTPUT
All test result expectations had a red cross next to them)
```

Now make it work! You only need to change the `Calculator` class to make the output "go green".

Aim to spend 30-60 minutes on the exercise. You might finish, you might not. But make sure you take notes as you go as we might chat about further enhancements to this code in an in person interview.

Feel free to use private methods, leave comments and use git as you wish.

Submit the code to andy@coveragebook.com as a single file named `gpa-test-yourgithubusername.rb`.

Andy
