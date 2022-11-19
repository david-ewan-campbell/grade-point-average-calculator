# CoverageBook Tech Test Exercise

## To run tests and see hopefully green passing test results
```
`ruby gpa-test.rb`
```

## Grade Point Average (GPA) 'Converter'

``` 
STEP ONE - Read through Instructions
```
[ORIGINAL INSTRUCTIONS](#original-instructions)

------
``` 
STEP TWO - See failing output by running...

`ruby gpa-test.rb`

Why are tests failing? 
- Just hard-coded 0 in gpa method & '' in announcement method
- No methods to iterate through and calculate required gpa
- Need to create a method to calculate a gpa from given test results
```
-------

``` 
STEP THREE - Changed code initially in 'gpa' & 'announcement' methods
- Get at least two expected test results turning 'green'
- Get visibility on where/what code needs to be added.
- Hard coded '4' and "Andy scored an average of 4.0" expectation 
from test array/out: 
- hash returns 2 green ticks in first test expectations for 'Andy'... 
```

---------- Andy ---------- \
✅ GPA: 4 \
✅ ANNOUNCEMENT: Andy scored an average of 4.0

### But rest of output of course returning failing tests i.e...

---------- Beryl ---------- \
❌ GPA: expected '3' but got '4' \
❌ ANNOUNCEMENT: expected 'Beryl scored an average of 3.0' but got 'Andy scored an average of 4.0'

```
STEP FOUR - Added a gpa_converter method
- Created a 1st hash pair from the given gpa scores list
of the 1st test expectation of the Andy's top score of 'A' => 4
- Added a method to iterate through grades and convert them to the equivalent score(a float) 
so they can be passed to the gpa method & added up & then 'announced'
- Added string statement in 'announcement' method to interpolate each 'local' instances
of 'name' & 'grades' that will be passed & mapped by the gpa converter method
```

### Result passes 'Andy' but rest return an error : 'nil can't be coerced into Float'
### Need to add rest of grades to score hash pairs to convert them.

-------

``` 
STEP FIVE - Added rest of gpa method hash pairs & a method to gpa 
in gpa_converter hash iteration to 'sum' the total
- The result has to be divided by the number of grades(exams taken)
to get the mean average of each gpa - example of some of the results...
```

---------- Chris ---------- \
✅ GPA: 2.5 \
✅ ANNOUNCEMENT: Chris scored an average of 2.5 

---------- Dan ---------- \
❌ GPA: expected '3.5' but got '3.466666666666667' \
❌ ANNOUNCEMENT: expected 'Dan scored an average of 3.5' but got 'Dan scored an average of 3.466666666666667'

```
- An even number of 'length' of results returned a correct response
but 3 results returning recurring decimal places.
- Wrapped 'gpa_converter.sum/grades.length' in brackets to return that value first
- Then added a 'round' up method (to 1 decimal place 
to return just the result to one decimal place)

- ALL TESTS GREEN AND PASSING!
```

### Move on to extra tests/edge-cases \
### -'# how_might_you_do_these ='

```
STEP SIX - Edge/extra test Cases:
- Moved one extra test/edge case into tests array to see what output error it returned.
- No data outgoing in the 'out:' hash for edge cases 
and no functions/methods to handle or return any response in gpa & announcement methods
- Added expectation to 1st outgoing hash for 'Non-grades' of 'nil' and an error warning
- After some research into how to pass 'exceptions' and alert for errors inputted
added a 'rescue' method to look for a nil input and pass to announcement method
to return an error message with an if else statement.

- All the gpa returns suddenly returned red
- Realised I hadn't instantiated a local @gpa = gpa instance
to make it available to use in the announcement method.
- Works!! First extra edge case passes...
```

```
#STEP SEVEN - Rest of edge-cases altered to give same output of nil and an error message.
BUT!!
- Is this just a quick fix? Should I have added the nil/error message output in the hash?
- Simplest fix to give something to calculator class/methods to get a response
and change methods to respond accordingly. 
- But there is probably a more elegant (and 'correct' solution for these extra test cases?)
but also would be much more complex I suspect!
- The best solution I felt I could find in the time available.
- Continue to work on this out of interest another time
and a very helpful exercise in working with a different code base
and work on confidence in changing and adapting it work.
```
## Some resources on methods used (add more...)
CALCULATING GPA \
https://studycrumb.com/how-to-calculate-gpa

COLLECT/MAP METHOD IN RUBY \
https://www.rubyinrails.com/2014/01/25/ruby-difference-between-collect-and-map/

FINDING THE MEAN AVERAGE FROM AN ARRAY IN RUBY \
https://andycroll.com/ruby/calculate-a-mean-average-from-a-ruby-array/

ROUNDING FLOAT TO NEAREST DECIMAL PLACE / .round method \
https://www.educative.io/answers/how-to-round-float-value-to-the-nearest-n-decimal-places-in-ruby

RESCUE EXCEPTIONS IN RUBY \
https://blog.appsignal.com/2018/04/10/rescuing-exceptions-in-ruby.html

-------------
-------------

# Original Instructions...


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

Submit the code to ------------ as a single file named `gpa-test-yourgithubusername.rb`.

Andy
