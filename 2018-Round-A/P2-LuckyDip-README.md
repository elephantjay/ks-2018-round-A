#### Problem
You are participating in the Grand Kickstart Lucky Dip with many fantastic and amazing prizes (and some not so good ones)!

In this Lucky Dip, there is a bag with **N** items. The i-th item in the bag has value **V<sub>i</sub>**. You will put your hand into the bag and draw one item at random; all items in the bag have an equal probability of being chosen. The organizers want contestants to feel that they have some element of choice, so after you draw an item, you can either keep it, or "redip" by returning it to the bag and drawing again. (Note that the returned item is now just as likely to be chosen as any of the other items in the bag.) You may only redip a maximum of **K** times. If you use **K** redips, you must keep the item that you draw on your (**K** + 1)-th draw.

If you play optimally to maximize the value of the item you will end the game with, what is the expected value of that item?

##### Input
The input starts with one line containing one integer **T**: the number of test cases. **T** test cases follow.

Each test case consists of two lines. The first line consists of two integers **N** and **K**: the number of items in the bag, and the maximum number of times you may redip. The second line consists of **N** integers **V<sub>i</sub>**, each representing the value of the i-th item.

##### Output
For each test case, output one line containing `Case #x: y`, where `x` is the test case number (starting from 1) and `y` is the expected value described above. Your answer will be considered correct if it is within an absolute or relative error of 10-6 of the correct answer. See the FAQ for an explanation of what that means, and what formats of real numbers we accept.

##### Limits
Memory limit: 1GB.
1 ≤ **T** ≤ 100.
1 ≤ **V<sub>i</sub>** ≤ 109.
1 ≤ **N** ≤ 2 * 104.

##### Small dataset (Test set 1 - Visible)
Time limit: 20 seconds.
0 ≤ **K** ≤ 1.

##### Large dataset (Test set 2 - Hidden)
Time limit: 60 seconds.
0 ≤ **K** ≤ 5 * 10^4^.

##### Sample  
| Input  | Output | 
| :--- | ---: |
| 5 | |
| 4 0 | Case #1: 2.500000 |
| 1 2 3 4 | Case #2: 6.000000 |
| 3 1 | Case #3: 80000.000000 |
| 1 10 1 | Case #4: 10.000000 |
| 3 15 | Case #5: 12.358400 |
| 80000 80000 80000 | |
| 1 1 | |
| 10 | |
| 5 3 | |
| 16 11 7 4 1 | |
  
In Sample Case #1, you cannot redip, so the expected value is just the mean of the items in the bag which is (1 + 2 + 3 + 4) / 4 = 2.5.

In Sample Case #2, the best strategy is to keep the item of value 10 if you get it, and redip otherwise. The chance of getting that item (on either the first or second draw) is 1 - (2/3)2 = 5/9, hence the expected value is (5/9 * 10) + (4/9 * 1) = 6.

In Sample Case #3, since all the items have the same value, it does not matter how many times you redip and hence the expected value is 80000.

Note that cases #3 and #5 would not appear in the Small dataset.