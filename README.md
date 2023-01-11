
# Eatery Simulation - Sup Dup at IIT Kharagpur





## Section 1: Description of the System

Sup Dup (Super Duper) is an eatery near Tech Market, inside the campus of IIT Kharagpur.
The restaurant is closed on Mondays. On the rest of the days of thee week, it opens at 10:00am
and closes at 9:30 pm. The eatery has 1 kitchen and multiple tables and servers. Preliminary
subjective analysis indicates that the restaurant is not very crowded.
## Section 2: Preliminary Analysis
Due to the fact that Super Duper is located away from the Academic Areas, conventional
wisdom would suggest that it does not experience high-traffic during lunch time on weekdays.
The abundance of eateries around 2.2, the circular path covering most Halls of Residence, has
caused many students to shun visiting Super Duper. However, one of the advantages it has
over other eateries is that it opens earlier in the morning than most of them.
## Section 3: Hypotheses
Based on the above analysis, we can construct 3 hypotheses, which will be tested using our
methodology.


1. Super Duper has lesser visitors during lunch time on weekdays compared to dinner time on weekdays.

2. Super Duper has lesser visitors during lunch time on weekdays compared to lunch time on weekends.

3. Super Duper has comparatively higher number of visitors in the mornings.

## Section 4: Other Questions
We would like to further study the system and derive insights on behalf of the owners of Super
Duper, by performing sensitivity analysis which can help them optimise their operations. We
would also like to learn more about the working of the Kitchen without entering it. This kind of
a black box analysis is extremely difficult to carry out. The questions we would like to answer
are:


1. What is the distribution of customers entering the restaurant based on day of the week and time?

2. What is the distribution of group size (people sitting on the same table) based on day of the week and time?

3. What are the average waiting times and average queue lengths based on day of the week and time?

4. What would happen if the number of tables is increased or decreased by 1? How would it affect average queue length, waiting time, and utilisation of servers?

5. What would happen if the number of servers is increased or decreased by 1? How would it affect average queue length, waiting time, and utilisation of tables?

6. What kind of a system is the kitchen? Is it a First-In-First-Out system? Is there parallel processing?

## Section 5: Methodology
We plan to visit Super Duper for seven continuous days in order to collect data for our analysis.
Each day, there will be 3 shifts for students to make their observations.
1. Breakfast - 10:00 am to 12:00 pm
2. Lunch - 12:00 pm to 3:30 pm
3. Snacks - 3:30 pm to 7:00 pm
4. Dinner - 7:00 pm to 10:00 pm

#### During each shift we collected information regarding:

• Inter-Arrival Time

• Number of people in a group

• Serving Time

• Exit Time

#### Data Analysis: 

The data for weekdays was combined and the data for Saturday was considered
separately. Thus we had to analyse 8 groups of data, based on weekday/weekend and the 4
shifts. For each group, a distribution of inter-arrival times was created using ARENA’s Input
Analyser Mean and Standard deviation were calculated for each group too Questions were
answered using these observations and the hypotheses were checked Serving time distributions
were also analysed using the Input Analyser Distribution of size of group was also analysed
using the Input Analyser.


## Section 6: Arena Simulation
### Model 1 - FiFo + Delay-Release
• Create Module - given Inter-arrival distribution (weekend lunch)\
• Process Module - Kitchen with Delay-Release type\
• Process module - Eating which waits for customer to finish eating\
• Dispose Module

#### Run for 3 hours
**Average queue length:** 4.1\
**Maximum Queue length:** 6\
**Average Wait time:** 6.8 mins

### Model 2 - FiFo + Seize Delay-Release
• Create Module - given Inter-arrival distribution (weekend lunch)\
• Process Module - Kitchen with Seize Delay-Release type\
• Process module - Eating which waits for customer to finish eating\
• Dispose Module

#### Run for 3 hours
**Average queue length:** 6.9\
**Maximum Queue length:** 11\
**Average Wait time:** 8.5 mins

### Model 3 - Hybrid + Delay-Release
• Create Module - given Inter-arrival distribution (weekend lunch)\
• Assign Module - Assign attribute (0 - tea/smoke break, 1 - meal/snack)\
• Decide Module - Whether the customer is arriving for tea break\
• Decide Module - Whether the queue is empty\
• Process Module - Kitchen with Seize Delay-Release type\
• Process module - Eating which waits for customer to finish eating\
• Dispose Module

#### Run for 3 hours
**Average queue length:** 3.4\
**Maximum Queue length:** 5\
**Average Wait time:** 5.7 mins

### Model 4 - Hybrid + Seize Delay-Release
• Create Module - given Inter-arrival distribution (weekend lunch)\
• Assign Module - Assign attribute (0 - tea/smoke break, 1 - meal/snack)\
• Decide Module - Whether the customer is arriving for tea break\
• Decide Module - Whether the queue is empty\
• Process Module - Kitchen with Seize Delay-Release type\
• Process module - Eating which waits for customer to finish eating\
• Dispose Module

#### Run for 3 hours
**Average queue length:** 5.8
**Maximum Queue length:** 8
**Average Wait time:** 7.7 mins
## Section 7: Results
### Hypotheses
• Hypothesis 1: Customers arrive every 7.02 minutes for lunch on weekdays, and every 6.75 minutes for dinner on weekdays.\
• Hence it can be accepted, but the surety is not high.\
• Hypothesis 2: Customers arrive every 7.02 minutes for lunch on weekdays, and every 5.36 minutes for lunch on weekends.\
• Hence it can be accepted with high surety.\
• Hypothesis 3: On both, weekends and weekdays, snacktime has the most frequent arrival by customers and the differences are significant in both. (more than 1 sigma)\
• Hence it can be accepted with high surety.

### Other Questions
• Distribution of customers can be said to follow a gamma distribution\
• Weekends show more frequent visits than weekdays in every shift\
• Most people come alone, some come in pairs and few come in larger groups\
• Average service time is around 5.86 minutes\
• The maximum queue length (number of people waiting to be served) was 5\
• The maximum number of groups seated was 8\
• Increasing the number of tables or servers will not increase the productivity as the limiting factor was the preparation of food in the kitchen\
• The kitchen seems to be a hybrid of FiFo system where customers with small orders are given preference or parallel service

## Section 8: Conclusion and Suggestions
• The kitchen (cooking process) is the limiting factor for customer waiting times and queue length\
• Thus, the owner could add one more stove in the kitchen (as staff seem to be free enough)\
• However, the waiting times and queue lengths are anyways low relative to other eateries like HJB/JCB/Smart Pind/VS and hence the focus should be on getting customers more frequently\
• Around 28% of customers were smokers who came to drink tea, thus the surrounding shops prove to be a boon.\
• The full capacity (10 tables) was never utilised and hence tables do not need to be added.\
• Greater utilisation of tables and servers will occur only if more customers enter
## Section 9: Figures

