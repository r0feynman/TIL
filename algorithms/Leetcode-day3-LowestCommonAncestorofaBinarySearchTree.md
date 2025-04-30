## 1. 문제 설명
Binary Search Tree(BST)에 임의의 노드 p와 q가 주어졌을 때 가장 낮은 공통 조상(LCA)를 찾는 문제

## 2. 문제 해결 접근 방법
#### bst의 특징
- root의 left node는 root 보다 작다.
- root의 right node는 root 보다 크다.
#### 1. bst의 특징을 이용하는 방법
- root에서 시작해서 p와 q가 root보다 작다면 왼쪽, root보다 크다면 오른쪽 서브트리에 있다고 볼 수 있다.
- 위 과정을 반복하다가 p < root < q 인 root가 lca

## 3. 문제 풀이


#### 반복을 이용한 해결
```python
class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        while root:
            if root.val > q.val and root.val > p.val:
                root = root.left
            elif root.val < q.val and root.val < p.val:
                root = root.right
            else:
                return root
```
63m, 20.89MB

#### 재귀적 해결법
```python
class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
    
	    if p.val < root.val > q.val:
            return self.lowestCommonAncestor(root.left, p, q)
        if p.val > root.val < q.val:
            return self.lowestCommonAncestor(root.right, p, q)
        return root
```

