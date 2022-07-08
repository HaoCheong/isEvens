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

## The Recursive way

Its recursion hence it must be good. Right?

```python
def isEven(num):
  while num >= 1:
    print(f"isEven({num})")
    num -= 2
  return (num == 0)
```

## The Mathematical Way

Mathematically proven

```python
def isEvenMuchBiggerBrain(num):
  '''
  Suppose x is an even number. This means we can write x = 2k for some integer k.
  '''
  for k in range(1,num/2):
    if (num == 2 * k):
      return True
  return False

def isEvenBiggestBrain(num):
  '''
  Proof by induction
  '''
  nums = [i for i in range(0, num, 2)]
  result = map(isEvenBigBrain, nums)
  return all(result) and num in nums
```
