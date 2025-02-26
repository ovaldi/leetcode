# [1470. Shuffle the Array](https://leetcode.com/problems/shuffle-the-array)

[中文文档](/solution/1400-1499/1470.Shuffle%20the%20Array/README.md)

## Description

<p>Given the array <code>nums</code> consisting of <code>2n</code> elements in the form <code>[x<sub>1</sub>,x<sub>2</sub>,...,x<sub>n</sub>,y<sub>1</sub>,y<sub>2</sub>,...,y<sub>n</sub>]</code>.</p>

<p><em>Return the array in the form</em> <code>[x<sub>1</sub>,y<sub>1</sub>,x<sub>2</sub>,y<sub>2</sub>,...,x<sub>n</sub>,y<sub>n</sub>]</code>.</p>

<p>&nbsp;</p>

<p><strong>Example 1:</strong></p>

<pre>

<strong>Input:</strong> nums = [2,5,1,3,4,7], n = 3

<strong>Output:</strong> [2,3,5,4,1,7] 

<strong>Explanation:</strong> Since x<sub>1</sub>=2, x<sub>2</sub>=5, x<sub>3</sub>=1, y<sub>1</sub>=3, y<sub>2</sub>=4, y<sub>3</sub>=7 then the answer is [2,3,5,4,1,7].

</pre>

<p><strong>Example 2:</strong></p>

<pre>

<strong>Input:</strong> nums = [1,2,3,4,4,3,2,1], n = 4

<strong>Output:</strong> [1,4,2,3,3,2,4,1]

</pre>

<p><strong>Example 3:</strong></p>

<pre>

<strong>Input:</strong> nums = [1,1,2,2], n = 2

<strong>Output:</strong> [1,2,1,2]

</pre>

<p>&nbsp;</p>

<p><strong>Constraints:</strong></p>

<ul>

    <li><code>1 &lt;= n &lt;= 500</code></li>

    <li><code>nums.length == 2n</code></li>

    <li><code>1 &lt;= nums[i] &lt;= 10^3</code></li>

</ul>

## Solutions

<!-- tabs:start -->

### **Python3**

```python
class Solution:
    def shuffle(self, nums: List[int], n: int) -> List[int]:
        ans = []
        for i in range(n):
            ans.append(nums[i])
            ans.append(nums[i + n])
        return ans
```

### **Java**

```java
class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] ans = new int[n << 1];
        for (int i = 0, j = 0; i < n; ++i) {
            ans[j++] = nums[i];
            ans[j++] = nums[i + n];
        }
        return ans;
    }
}
```

### **TypeScript**

```ts
function shuffle(nums: number[], n: number): number[] {
    let ans = [];
    for (let i = 0; i < n; i++) {
        ans.push(nums[i], nums[n + i]);
    }
    return ans;
}
```

### **C++**

```cpp
class Solution {
public:
    vector<int> shuffle(vector<int>& nums, int n) {
        vector<int> ans;
        for (int i = 0; i < n; ++i) {
            ans.push_back(nums[i]);
            ans.push_back(nums[i + n]);
        }
        return ans;
    }
};
```

### **Go**

```go
func shuffle(nums []int, n int) []int {
	var ans []int
	for i := 0; i < n; i++ {
		ans = append(ans, nums[i])
		ans = append(ans, nums[i+n])
	}
	return ans
}
```

### **...**

```

```

<!-- tabs:end -->
