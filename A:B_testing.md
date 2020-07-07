# A/B testing

**Test preparation consists of two tasks:**

- planning: how long it should be, how we will divide into groups, find good metrics
- check results

**Types of Metrics:**

- Online: wait a long time for results (money earned, customer activity)
- Online:  gather statistics quickly (button click, product purchase)
- Offline: older histirical data, experiments whic you can calculate offline.

**Sampling (must be representative!!!):**

* stratification: choose samples by main rules: adge, sex, city, income and etc.
* randomization: choose samples fully randomly -- the samples will be the same for all social / demographic indicators
* related samples: conducts an experiment twice on the same client group. To avoid bias due to the order of the tests, one half of the group first give the first test, then the second, second half the other way around.

**Sustainability:**

* Reverse experiment:
  * Conduct A/B test
  * For example, new idea shows better results
  * Change 90% to new idea, 10% save with old one
  * Continue test
* A/A testing: divided into groups,  show the same idea to the groups. If the groups are well selected, we will not see the result on them.

**Design:**

* Choose $\alpha$ and $\beta$
* Calculate appropriate $n$, using the size of the result you want to measure