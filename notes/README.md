# Notes

This folder is optional.

Use it for your own:
- checkpoint-question answers;
- predictions;
- complexity notes;
- debugging notes;
- reflections.

You do not need to keep formal notes unless a lab specifically asks you to.

Lab 0:

1. Which of the three operations may need to inspect every player?
    FindHighestsScore has to loop through every element in the list to get the highest score. The others may loop through through 
    every element in the list, and then return false or null, as a worst-case.

2. If the number of players becomes 100 times larger, which operation(s) do you expect to become noticeably more expensive?
    Since FindHighestScore always has to loop over the entire collection, I would expect that one to become noticeably more expensive.
    That being said, all methods are at worst O(n), however, FindHighestScore's only case of being O(1) is if the list is empty.
    The other methods can exit early.

3. What information could we organize differently if finding players by ID became extremely common?
    We could turn the collection into a dictionary. Since ID is unique, that could work as the key. That way, the FindById could simply do return _players[id]

4. What edge case did you choose to test, and why?
    I tested the case sensitivity given that was in the lab instructions.

5. At what point did you make a Git commit? What made that a sensible checkpoint?
    After every step. So after implementing each function, and then after writing and running the new test.
    And I will commit after this, too.

# Lab 1:

Task 1

1. What does i represent?
    i represents the current index that is being compared to target.

2. When does the method stop early?
    When it finds a value at an index that matches the target.

3. What does -1 mean?
    That it didn't find a value matching the target.

4. What is the best case?
    That it finds a value matching target on index 0.

5. What is the worst case?
    That it iterates over the whole collection without finding the target or finding the target
    at the very last index.

6. If the array becomes twice as large, what happens to the worst-case amount of work?
    It also becomes twice as large. The method is O(n) time complexity.

Task 2

Binary search only works with ordered data because it relies on the order of the values
 to determine which half of the data to discard. Without ordered data, there would be no
 way to guarantee that the target wasn't in the discarded half.


