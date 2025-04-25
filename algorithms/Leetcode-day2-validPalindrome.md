# 1. 문제 설명
유효한 회문 문제(특수문자, 공백을 제거하고 회문인지 검사하는 문제)

# 2. 아이디어
##### 공백, 특수문자, 기호 등을 제거하고 뒤집어도 같은가

# 3. 문제 풀이
```python
import re

def is_palindrome(s:str) -> bool:
	s = re.sub(^[a-zA-Z0-9], "", s).lower()
	# re.sub(pattern, replace, string)
	
	return s == s[::-1]
```

- re func
	- re.match(pattern, string)
	- re.sub(pattern, replace, string)
	- re.findall(pattern, string)
	- re.split(pattern, string)
	- re.finditer(pattern, string)
	- re.search(pattern, string)
