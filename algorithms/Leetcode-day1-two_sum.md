
## 1. 문제 설명
- nums 가 주어졌을 때 target이 되는 두 수의 인덱스를 반환하는 문제
- 각 요소는 한 번만 사용 가능
- target이 되는 두 수는 반드시 존재

## 2. 아이디어
- index 함수를 이용하는 법
- dict mapping을 이용하는 법

## 3. 문제 풀이
```python
class Solution:

    def twoSum(self, nums: List[int], target: int) -> List[int]:
    #     for num in nums:
    #         complement = target - num
    #         if complement in nums[nums.index(num)+1:]:
    #             return [nums.index(num), nums[nums.index(num)+1:].index(complement)+nums.index(num)+1]

        num_to_index = dict()
        for idx, num in enumerate(nums):
            complement = target - num
            if complement in num_to_index:
                return [num_to_index[complement], idx]
                
            num_to_index[num] = idx
```
