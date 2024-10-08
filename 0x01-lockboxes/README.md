0x01. Lockboxes
Description
You have n locked boxes in front of you. Each box is numbered sequentially from 0 to n - 1. Each box may contain keys to other boxes. This method determines if all boxes can be opened, starting from the first box, which is already unlocked.

Requirements
Write a function canUnlockAll(boxes) that determines if all boxes can be unlocked.

Prototype: def canUnlockAll(boxes)
Input:
boxes is a list of lists, where each sublist represents a box and contains integers representing keys to other boxes.
A key with the same number as a box opens that box.
Assume all keys are positive integers.
There can be keys that do not have corresponding boxes.
Output:
Return True if all boxes can be opened.
Return False if there are any boxes that cannot be opened.
boxes = [[1], [2], [3], [4], []]
print(canUnlockAll(boxes))  # Output: True
In this example, starting from box 0, you can sequentially unlock all other boxes.
