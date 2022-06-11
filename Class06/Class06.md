## How to use Random Module

> Randint

If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.

> Random

If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:

import random
random.random() * 100

> Choice

Generate a random value from the sequence sequence.

random.choice( ['red', 'black', 'green'] ).
The choice function can often be used for choosing a random element from a list.
 
> Shuffle

The shuffle function, shuffles the elements in list in place, so they are in a random order.

> Randrange

Generate a randomly selected element from range(start, stop, step)




## What is Risk Analysis

The probability of any unwanted incident is defined as Risk. In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

- Why use Risk Analysis?

In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

Possible Risks:
1. Use of new hardware
2. Use of new technology
3. Use of new automation tool
4. The sequence of code
5. Availability of test resources for the application

There are certain risks that are unavoidable:
1. The time that you allocated for testing
2. A defect leakage due to the complexity or size of the application
3. Urgency from the clients to deliver the project
4. Incomplete requirements

In such cases, you have to tackle the situation with care. Following points can be taken care of:
1. Conduct Risk Assessment review meeting
2. Use maximum resources to work on high-risk areas
3. Create a Risk Assessment database for future use
4. Identify and notice the risk magnitude indicators: high, medium, low.

*High*: means the effect of the risk would be very high and non-tolerable. The company might face loss.

*Medium*: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

*Low*: it is tolerable. There lies little or no external exposure or no financial loss.

- Risk Identification

There are different sets of risks included in the risk identification process. Those are as follows:

1. Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

2. Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

3. Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

4. Software Risks: You should be well versed with the risks associated with the software development process.

- Risk Assessment

In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically.

- The perspective of Risk Assessment

1. Effect >> To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.
2. Cause >> To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.
3. Likelihood >> To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.


## Test Coverage

If you make a certain level of coverage a target, people will try to attain it. The trouble is that high coverage numbers are too easy to reach with low quality testing. At the most absurd level you have AssertionFreeTesting. But even without that you get lots of tests looking for things that rarely go wrong distracting you from testing the things that really matter.

Like most aspects of programming, testing requires thoughtfulness. TDD is a very useful, but certainly not sufficient, tool to help you get good tests. If you are testing thoughtfully and well, I would expect a coverage percentage in the upper 80s or 90s. I would be suspicious of anything like 100% - it would smell of someone writing tests to make the coverage numbers happy, but not thinking about what they are doing.

The reason, of course, why people focus on coverage numbers is because they want to know if they are testing enough. Certainly low coverage numbers, say below half, are a sign of trouble. But high numbers don't necessarily mean much, and lead to ignorance-promoting dashboards. Sufficiency of testing is much more complicated attribute than coverage can answer.
