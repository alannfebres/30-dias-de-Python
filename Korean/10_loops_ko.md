<div align="center">   <h1> 30 Days Of Python: Day 10 - Loops</h1>   <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">   <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&amp;logo=linkedin&amp;style=social">   </a>   <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">   <img src="https://img.shields.io/twitter/follow/asabeneh?style=social" alt="Twitter Follow">   </a>
</div>
<p data-md-type="paragraph"><sub data-md-type="raw_html">Author: <a data-md-type="raw_html" href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br> <small data-md-type="raw_html"> Second Edition: July, 2021</small></sub></p>
<div data-md-type="block_html"></div>

[&lt;&lt; Day 9](../09_Day_Conditionals/09_conditionals.md) | [Day 11 &gt;&gt;](../11_Day_Functions/11_functions.md)

![30DaysOfPython](../images/30DaysOfPython_banner3@2x.png)

- [π Day 10](#-day-10)
    - [Loops](#loops)
        - [While λ£¨ν](#while-λ£¨ν)
        - [Break κ³Ό Continue - Part 1](#break-κ³Ό-continue---part-1)
        - [For λ£¨ν](#for-λ£¨ν)
        - [Break κ³Ό Continue - Part 2](#break-κ³Ό-continue---part-2)
        - [λ²μ κΈ°λ₯](#λ²μ-κΈ°λ₯)
        - [μ€μ²© For λ£¨ν](#μ€μ²©-for-λ£¨ν)
        - [For Else](#for-else)
        - [Pass](#pass)
    - [π» Exercises: Day 10](#-exercises-day-10)
        - [Exercises: Level 1](#exercises-level-1)
        - [Exercises: Level 2](#exercises-level-2)
        - [Exercises: Level 3](#exercises-level-3)

# π Day 10

## Loops

μΈμμ μΌμμΌλ‘ κ°λ μ°¨ μμ΅λλ€. νλ‘κ·Έλλ°μμ μ°λ¦¬λ λν λ§μ λ°λ³΅ μμμ μνν©λλ€. λ°λ³΅ μμμ μ²λ¦¬νκΈ° μν΄ νλ‘κ·Έλλ° μΈμ΄λ λ£¨νλ₯Ό μ¬μ©ν©λλ€. Python νλ‘κ·Έλλ° μΈμ΄λ λν λ€μ μ νμ λ λ£¨νλ₯Ό μ κ³΅ν©λλ€.

1. while loop
2. for loop

### While λ£¨ν

μ°λ¦¬λ while λ£¨νλ₯Ό λ§λ€κΈ° μν΄ μμ½μ΄ *while* μ μ¬μ©ν©λλ€. μ£Όμ΄μ§ μ‘°κ±΄μ΄ λ§μ‘±λ  λκΉμ§ λ¬Έ λΈλ‘μ λ°λ³΅μ μΌλ‘ μ€ννλ λ° μ¬μ©λ©λλ€. μ‘°κ±΄μ΄ κ±°μ§μ΄ λλ©΄ λ£¨ν λ€μ μ½λ νμ΄ κ³μ μ€νλ©λλ€.

```py
  # syntax
while condition:
    code goes here
```

**μμ:**

```py
count = 0
while count < 5:
    print(count)
    count = count + 1
#prints from 0 to 4
```

μμ while λ£¨νμμ countκ° 5μΌ λ μ‘°κ±΄μ΄ falseκ° λ©λλ€. μ΄λ λ£¨νκ° μ€μ§λ©λλ€. μ‘°κ±΄μ΄ λ μ΄μ μ°Έμ΄ μλ λ μ½λ λΈλ‘μ μ€ννκ³  μΆλ€λ©΄ *else* λ₯Ό μ¬μ©ν  μ μμ΅λλ€.

```py
  # syntax
while condition:
    code goes here
else:
    code goes here
```

**μμ:**

```py
count = 0
while count < 5:
    print(count)
    count = count + 1
#prints from 0 to 4
```

μμ λ£¨ν μ‘°κ±΄μ countκ° 5μ΄κ³  λ£¨νκ° μ€μ§λκ³  μ€νμ΄ else λ¬Έμ μμνλ©΄ κ±°μ§μ΄ λ©λλ€. κ²°κ³Όμ μΌλ‘ 5κ° μΈμλ©λλ€.

### Break κ³Ό Continue - Part 1

- μ€λ¨: λ£¨νμμ λ²μ΄λκ±°λ μ€λ¨νκ³  μΆμ λ μ€λ¨μ μ¬μ©ν©λλ€.

```py
# syntax
while condition:
    code goes here
    if another_condition:
        break
```

**μμ:**

```py
count = 0
while count < 5:
    print(count)
    count = count + 1
    if count == 3:
        break
```

μμ while λ£¨νλ 0, 1, 2λ§ μΈμνμ§λ§ 3μ λλ¬νλ©΄ μ€μ§ν©λλ€.

- κ³μ: continue λ¬Έμ μ¬μ©νλ©΄ νμ¬ λ°λ³΅μ κ±΄λλ°κ³  λ€μμ κ³μν  μ μμ΅λλ€.

```py
  # syntax
while condition:
    code goes here
    if another_condition:
        continue
```

**μμ:**

```py
count = 0
while count < 5:
    if count == 3:
        continue
    print(count)
    count = count + 1
```

μμ while λ£¨νλ 0, 1, 2 λ° 4λ§ μΈμν©λλ€(3μ κ±΄λλλλ€).

### For λ£¨ν

*for* ν€μλλ λ€λ₯Έ νλ‘κ·Έλλ° μΈμ΄μ μ μ¬νμ§λ§ κ΅¬λ¬Έμ΄ μ½κ° λ€λ₯Έ for λ£¨νλ₯Ό λ§λλ λ° μ¬μ©λ©λλ€. λ£¨νλ μνμ€(μ¦, λͺ©λ‘, νν, μ¬μ , μ§ν© λλ λ¬Έμμ΄)λ₯Ό λ°λ³΅νλ λ° μ¬μ©λ©λλ€.

- For loop with list

```py
# syntax
for iterator in lst:
    code goes here
```

**μμ:**

```py
numbers = [0, 1, 2, 3, 4, 5]
for number in numbers: # number is temporary name to refer to the list's items, valid only inside this loop
    print(number)       # the numbers will be printed line by line, from 0 to 5
```

- For loop with string

```py
# syntax
for iterator in string:
    code goes here
```

**μμ:**

```py
language = 'Python'
for letter in language:
    print(letter)


for i in range(len(language)):
    print(language[i])
```

- For loop with tuple

```py
# syntax
for iterator in tpl:
    code goes here
```

**μμ:**

```py
numbers = (0, 1, 2, 3, 4, 5)
for number in numbers:
    print(number)
```

- μ¬μ μ μ¬μ©ν For λ£¨ν μ¬μ μ ν΅ν λ£¨νλ μ¬μ μ ν€λ₯Ό μ κ³΅ν©λλ€.

```py
  # syntax
for iterator in dct:
    code goes here
```

**μμ:**

```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
}
for key in person:
    print(key)

for key, value in person.items():
    print(key, value) # this way we get both keys and values printed out
```

- Loops in set

```py
# syntax
for iterator in st:
    code goes here
```

**μμ:**

```py
it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
for company in it_companies:
    print(company)
```

### Break κ³Ό Continue - Part 2

μ§§μ μλ¦Ό: *μ€λ¨* : λ£¨νκ° μλ£λκΈ° μ μ μ€λ¨νκ³  μΆμ λ μ€λ¨μ μ¬μ©ν©λλ€.

```py
# syntax
for iterator in sequence:
    code goes here
    if condition:
        break
```

**μμ:**

```py
numbers = (0,1,2,3,4,5)
for number in numbers:
    print(number)
    if number == 3:
        break
```

μμ μμμ λ£¨νλ 3μ λλ¬νλ©΄ μ€μ§λ©λλ€.

κ³μ: λ£¨ν λ°λ³΅μμ μΌλΆ λ¨κ³λ₯Ό κ±΄λλ°κ³  μΆμ λ κ³μμ μ¬μ©ν©λλ€.

```py
  # syntax
for iterator in sequence:
    code goes here
    if condition:
        continue
```

**μμ:**

```py
numbers = (0,1,2,3,4,5)
for number in numbers:
    print(number)
    if number == 3:
        continue
    print('Next number should be ', number + 1) if number != 5 else print("loop's end") # for short hand conditions need both if and else statements
print('outside the loop')
```

μμ μμμ μ«μκ° 3μ΄λ©΄ μ‘°κ±΄ *λ€μ* λ¨κ³(λ£¨ν λ΄λΆ)λ₯Ό κ±΄λλ°κ³  λ°λ³΅μ΄ λ¨μ μμΌλ©΄ λ£¨ν μ€νμ΄ κ³μλ©λλ€.

### λ²μ κΈ°λ₯

*range()* ν¨μλ μ«μ λͺ©λ‘μ μ¬μ©λ©λλ€. *λ²μ(μμ, λ, λ¨κ³)* λ μμ, μ’λ£ λ° μ¦λΆμ μΈ κ°μ§ λ§€κ°λ³μλ₯Ό μ¬μ©ν©λλ€. κΈ°λ³Έμ μΌλ‘ 0λΆν° μμνκ³  μ¦λΆμ 1μλλ€. λ²μ μνμ€μλ μ΅μ 1κ°μ μΈμ(μ’λ£)κ° νμν©λλ€. λ²μλ₯Ό μ¬μ©νμ¬ μνμ€ λ§λ€κΈ°

```py
lst = list(range(11))
print(lst) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
st = set(range(1, 11))    # 2 arguments indicate start and end of the sequence, step set to default 1
print(st) # {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

lst = list(range(0,11,2))
print(lst) # [0, 2, 4, 6, 8, 10]
st = set(range(0,11,2))
print(st) #  {0, 2, 4, 6, 8, 10}
```

```py
# syntax
for iterator in range(start, end, step):
```

**μμ:**

```py
for number in range(11):
    print(number)   # prints 0 to 10, not including 11
```

### μ€μ²© For λ£¨ν

λ£¨ν μμ λ£¨νλ₯Ό μμ±ν  μ μμ΅λλ€.

```py
# syntax
for x in y:
    for t in x:
        print(t)
```

**μμ:**

```py
person = {
    'first_name': 'Asabeneh',
    'last_name': 'Yetayeh',
    'age': 250,
    'country': 'Finland',
    'is_marred': True,
    'skills': ['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address': {
        'street': 'Space street',
        'zipcode': '02210'
    }
}
for key in person:
    if key == 'skills':
        for skill in person['skills']:
            print(skill)
```

### For Else

λ£¨νκ° λλ  λ λ©μμ§λ₯Ό μ€ννλ €λ©΄ elseλ₯Ό μ¬μ©ν©λλ€.

```py
# syntax
for iterator in range(start, end, step):
    do something
else:
    print('The loop ended')
```

**μμ:**

```py
for number in range(11):
    print(number)   # prints 0 to 10, not including 11
else:
    print('The loop stops at', number)
```

### Pass

Pythonμμ when λ¬Έμ΄ νμνμ§λ§(μΈλ―Έμ½λ‘  λ€μ) μ½λλ₯Ό μ€ννλ κ²μ μ’μνμ§ μμΌλ―λ‘ μ€λ₯λ₯Ό νΌνκΈ° μν΄ *pass* λΌλ λ¨μ΄λ₯Ό μΈ μ μμ΅λλ€. λν ν₯ν μ§μ μ μν΄ μλ¦¬ νμμλ‘ μ¬μ©ν  μ μμ΅λλ€.

**μμ:**

```py
for number in range(6):
    pass
```

π λΉμ μ ν° μ΄μ νλ₯Ό μΈμ κ³ , λΉμ μ λ©μΆ μ μμ΅λλ€. κ³μνμΈμ! 10μΌμ°¨ μ±λ¦°μ§λ₯Ό λ°©κΈ μλ£νμΌλ©° μλν¨μ ν₯ν 10λ¨κ³λ₯Ό μλκ³  μμ΅λλ€. μ΄μ  λμ κ·Όμ‘μ μν λͺ κ°μ§ μ΄λμ νμ­μμ€.

## π» Exercises: Day 10

### Exercises: Level 1

1. for λ£¨νλ₯Ό μ¬μ©νμ¬ 0μμ 10κΉμ§ λ°λ³΅νκ³  while λ£¨νλ₯Ό μ¬μ©νμ¬ λμΌν μμμ μνν©λλ€.

2. for λ£¨νλ₯Ό μ¬μ©νμ¬ 10μμ 0κΉμ§ λ°λ³΅νκ³  while λ£¨νλ₯Ό μ¬μ©νμ¬ λμΌν μμμ μνν©λλ€.

3. print()λ₯Ό 7λ² νΈμΆνλ λ£¨νλ₯Ό μμ±νμ¬ λ€μ μΌκ°νμ μΆλ ₯ν©λλ€.

    ```py
      #
      ##
      ###
      ####
      #####
      ######
      #######
    ```

4. μ€μ²© λ£¨νλ₯Ό μ¬μ©νμ¬ λ€μμ λ§λ­λλ€.

    ```sh
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    # # # # # # # #
    ```

5. λ€μ ν¨ν΄μ μΈμν©λλ€.

    ```sh
    0 x 0 = 0
    1 x 1 = 1
    2 x 2 = 4
    3 x 3 = 9
    4 x 4 = 16
    5 x 5 = 25
    6 x 6 = 36
    7 x 7 = 49
    8 x 8 = 64
    9 x 9 = 81
    10 x 10 = 100
    ```

6. for λ£¨νλ₯Ό μ¬μ©νμ¬ ['Python', 'Numpy','Pandas','Django', 'Flask'] λͺ©λ‘μ λ°λ³΅νκ³  ν­λͺ©μ μΆλ ₯ν©λλ€.

7. for λ£¨νλ₯Ό μ¬μ©νμ¬ 0μμ 100κΉμ§ λ°λ³΅νκ³  μ§μλ§ μΆλ ₯

8. for λ£¨νλ₯Ό μ¬μ©νμ¬ 0μμ 100κΉμ§ λ°λ³΅νκ³  νμλ§ μΆλ ₯

### Exercises: Level 2

1. for λ£¨νλ₯Ό μ¬μ©νμ¬ 0μμ 100κΉμ§ λ°λ³΅νκ³  λͺ¨λ  μ«μμ ν©κ³λ₯Ό μΈμν©λλ€.

```sh
The sum of all numbers is 5050.
```

1. for λ£¨νλ₯Ό μ¬μ©νμ¬ 0μμ 100κΉμ§ λ°λ³΅νκ³  λͺ¨λ  μ§μμ ν©κ³Ό λͺ¨λ  μΉμ°μ ν©μ μΈμν©λλ€.

    ```sh
    The sum of all evens is 2550. And the sum of all odds is 2500.
    ```

### Exercises: Level 3

1. λ°μ΄ν° ν΄λλ‘ μ΄λνμ¬ [countries.py](https://github.com/Asabeneh/30-Days-Of-Python/blob/master/data/countries.py) νμΌμ μ¬μ©ν©λλ€. κ΅­κ°λ₯Ό μννκ³  λ¨μ΄ *land* λ₯Ό ν¬ν¨νλ λͺ¨λ  κ΅­κ°λ₯Ό μΆμΆν©λλ€.
2. μ΄κ²μ κ³ΌμΌ λͺ©λ‘μλλ€. ['banana', 'orange', 'mango', 'lemon'] λ£¨νλ₯Ό μ¬μ©νμ¬ μμλ₯Ό λ€μ§μ΅λλ€.
3. λ°μ΄ν° ν΄λλ‘ μ΄λνμ¬ [countries_data.py](https://github.com/Asabeneh/30-Days-Of-Python/blob/master/data/countries-data.py) νμΌμ μ¬μ©ν©λλ€.
    1. λ°μ΄ν°μ μ΄ μΈμ΄ μλ μΌλ§μλκΉ?
    2. λ°μ΄ν°μμ κ°μ₯ λ§μ΄ μ¬μ©λλ 10κ° μΈμ΄ μ°ΎκΈ°
    3. μΈκ³μμ μΈκ΅¬κ° κ°μ₯ λ§μ 10κ° κ΅­κ° μ°ΎκΈ°

π μΆνν©λλ€! π

[&lt;&lt; Day 9](../09_Day_Conditionals/09_conditionals.md) | [Day 11 &gt;&gt;](../11_Day_Functions/11_functions.md)
