# isEvens
"Writing bad code can only be achieve through deep knowledge of good code" ~ Socrates (Maybe)


## Canonical Way 

Boring, simple, standard. Weak.

```python
def isEven(num):
  return num % 2 == 0
```

## The Typecast Way:

Floats? What floats?

```python
def isEven(num):
  return int(num / 2) == num / 2
```

## The Loop way

Just leave it, and grab a cup of tea

```python
def isEven(num):
  while num >= 1:
    print(f"isEven({num})")
    num -= 2
  return (num == 0)
```

## The Mathematical Way

Proved by induction, hence it makes it smarter

```python
def isEven(num):
  '''
  Suppose x is an even number. This means we can write x = 2k for some integer k.
  '''
  for k in range(1,num/2):
    if (num == 2 * k):
      return True
  return False

def isEvenInduction(num):
  '''
  Proof by induction
  '''
  nums = [i for i in range(0, num, 2)]
  result = map(isEvenBigBrain, nums)
  return all(result) and num in nums
```

## The Last Character Way:

This one will actually work with negative numbers!

```python
def isEven(num):
  possible_endings = ['0','2','4','6','8']
  last_char = str(num)[-1]
  if last_char in possible_endings:
    return True
  return False
```

## Recursive way

Recursion depth is merely recommendation.

```python
def isEven(num):
  if (num == 0):
    return True
  elif (num == 1):
    return False
  else:
    return isEven(int(num)-2)
```
