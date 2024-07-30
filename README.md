# LEETCODE-Strings-1653
Sure, let's do a dry run of the `minimumDeletions` method in the `Solution` class. We'll use an example input string to understand how the function works step-by-step.

### Example Input:
Let's consider the input string `s = "baabaa"`.

### Initial Setup:
- `dp` (to keep track of the minimum deletions needed to make the substring balanced) is initialized to 0.
- `countB` (to keep track of the number of 'b' characters encountered so far) is initialized to 0.

### Step-by-Step Dry Run:

1. **Iteration 1:**
   - `c = 'b'`
   - Since `c` is 'b', increment `countB`.
   - `countB` becomes 1.
   - `dp` remains 0 because no 'a' is encountered.

   State after iteration 1:
   - `dp = 0`
   - `countB = 1`

2. **Iteration 2:**
   - `c = 'a'`
   - Since `c` is 'a', update `dp` to be the minimum of `dp + 1` and `countB`.
   - `dp = min(0 + 1, 1) = 1`.

   State after iteration 2:
   - `dp = 1`
   - `countB = 1`

3. **Iteration 3:**
   - `c = 'a'`
   - Since `c` is 'a', update `dp` to be the minimum of `dp + 1` and `countB`.
   - `dp = min(1 + 1, 1) = 1`.

   State after iteration 3:
   - `dp = 1`
   - `countB = 1`

4. **Iteration 4:**
   - `c = 'b'`
   - Since `c` is 'b', increment `countB`.
   - `countB` becomes 2.
   - `dp` remains 1 because no 'a' is encountered.

   State after iteration 4:
   - `dp = 1`
   - `countB = 2`

5. **Iteration 5:**
   - `c = 'a'`
   - Since `c` is 'a', update `dp` to be the minimum of `dp + 1` and `countB`.
   - `dp = min(1 + 1, 2) = 2`.

   State after iteration 5:
   - `dp = 2`
   - `countB = 2`

6. **Iteration 6:**
   - `c = 'a'`
   - Since `c` is 'a', update `dp` to be the minimum of `dp + 1` and `countB`.
   - `dp = min(2 + 1, 2) = 2`.

   State after iteration 6:
   - `dp = 2`
   - `countB = 2`

### Final State:
- `dp = 2`
- `countB = 2`

### Output:
The minimum number of deletions required to make the string "baabaa" balanced (all 'a's appear before all 'b's) is `2`.

So, the function will return `2` for the input string `s = "baabaa"`.
