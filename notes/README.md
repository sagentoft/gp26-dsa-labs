# Notes

This folder is optional.

Use it for your own:
- checkpoint-question answers;
- predictions;
- complexity notes;
- debugging notes;
- reflections.

You do not need to keep formal notes unless a lab specifically asks you to.

Lab 1:

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
