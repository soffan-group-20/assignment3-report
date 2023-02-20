# Report for assignment 3

This is a template for your report. You are free to modify it as needed.
It is not required to use markdown for your report either, but the report
has to be delivered in a standard, cross-platform format.

## Project

Name: Teammates

URL: https://github.com/TEAMMATES/teammates

TEAMMATES is a free online tool for managing peer evaluations and other feedback paths of your students. It is provided as a cloud-based service for educators/students and is currently used by hundreds of universities across the world.

## Onboarding experience

There were some issues, but eventually all team members managed to get the problem up and running.

For specific accounts of onboarding experiences refer to this issue: https://github.com/soffan-group-20/teammates/issues/1.

## Complexity

<!-- 1. What are your results for ten complex functions?
   * Did all methods (tools vs. manual count) get the same result?
   * Are the results clear?
2. Are the functions just complex, or also long?
3. What is the purpose of the functions?
4. Are exceptions taken into account in the given measurements?
5. Is the documentation clear w.r.t. all the possible outcomes? -->

We found 10 functions of cyclic complexity higher than 10. Some functions are complex, while others just have many branches. The functions handle things such as filtering, predicates, aggregation. The code doesn't use exceptions. The documentation for these functions was extremely bad, and many assumptions had to be made of the expected behavior of the functions.

## Refactoring

<!-- Plan for refactoring complex code:

Estimated impact of refactoring (lower CC, but other drawbacks?).

Carried out refactoring (optional, P+):

git diff ... -->

To refactor we simply extracted common blocks of behavior into other smaller functions, in order to reduce the CC and LOC of the functions. We managed to reduce the CC by 35% for all team members assigned functions.

Refactoring is done here:

- https://github.com/soffan-group-20/teammates/pull/18
- https://github.com/soffan-group-20/teammates/pull/14
- https://github.com/soffan-group-20/teammates/pull/48

## Coverage

### Tools

<!-- Document your experience in using a "new"/different coverage tool.

How well was the tool documented? Was it possible/easy/difficult to
integrate it with your build environment? -->

To get the coverage we simply ran the command `npm run coverage`. The coverage report was genererated as a HTML page which was easily parsable.

### Your own coverage tool

<!-- Show a patch (or link to a branch) that shows the instrumented code to
gather coverage measurements.

The patch is probably too long to be copied here, so please add
the git command that is used to obtain the patch instead:

git diff ... -->

Our own coverage tool was created by keeping track in a `Record<number, boolean>` object which branches were visited.

https://github.com/soffan-group-20/teammates/pull/15

<!-- What kinds of constructs does your tool support, and how accurate is
its output? -->

The tool doesn't support anything other than letting the programmer manually identifying branches and having to assign to the branch hashmap which branches were visited. The output is as accurate as the programmer allowed it to be.

### Evaluation

<!-- 1. How detailed is your coverage measurement?

2. What are the limitations of your own tool?

3. Are the results of your tool consistent with existing coverage tools? -->

Depending on how good the programmer placed the assignments to the hashmap, the tool can be just as good as existing coverage tools.

## Coverage improvement

<!-- Show the comments that describe the requirements for the coverage.
Report of old coverage: [link]
Report of new coverage: [link]
Test cases added:
git diff ...
Number of test cases added: two per team member (P) or at least four (P+). -->

https://github.com/soffan-group-20/teammates/issues/9#issuecomment-1436722422

## Self-assessment: Way of working

<!-- Current state according to the Essence standard: ...
Was the self-assessment unanimous? Any doubts about certain items?
How have you improved so far?
Where is potential for improvement? -->

The states Principles Established and Foundations Established were reached at our first meeting as we read the assignment requirements and decided on a plan for which project to focus on. We decided on a GitHub PR-based workflow. We reached the In Use state (by definition) once we started working on the project in our GitHub repository. Since then, we have been continually inspecting and adapting the tools we use. Since every team member has adopted our current tools and practices, and are involved in improving them, we are currently in the In Place state. The way of working might not feel fully natural yet, but we anticipate reaching the Working Well state some time during the next assignments.

Self assessment: https://github.com/soffan-group-20/teammates/issues/24

## Overall experience

<!-- What are your main take-aways from this project? What did you learn?

Is there something special you want to mention here? -->
