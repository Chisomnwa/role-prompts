# Exercise 2: Role-Based Mentoring and Feedback
**Objective: Use role-based prompts for personalized feedback.**

Ask the model to act as a coding mentor.

Provide a simple piece of code (e.g., a Python function with a bug).

Prompt the model: "Act as a mentor reviewing this code. Provide corrections and explain improvements."

Review the response and check if the role influences feedback style.

------
### My Answers

THis below Python code is used to find the index positions of the two numbers in an array that sums to a given number.

```python
def two_sum(nums, target):

    for i in range(len(nums)):
        for j in range(i +1, len(nums)):
            if nums[i] + nums[j] == target
                return [i, j]

    return None

if __name__ == "__main__":
    nums = [2, 7, 11, 15]
    target = 9
    print(two_sum(nums, target))
```
----
So, it gave me a technical laydown and detailed explanation of my errors, and this includes a constructive feedback on my approach, and the reasons behind my wrong implementation. It also gave me the correct approach to tackle the particular problem which is using a hash map approach. 

This new approach:

- is better for large datasets
- has a decreased time and space complexity

So, here is the correct code that solves the two sum problem:

```python
def two_sums(nums, target):
    seen = {}

    for i in range(len(nums)):
        complement = target - nums[i]

        if complement in seen:
            return [seen[complement], i]

            seen[nums[i]] = i

        return none

```