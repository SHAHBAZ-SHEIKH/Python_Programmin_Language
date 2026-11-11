# Python: User Input, Type Casting, Strings, Comparison & Logical Operators

> **Note:** Is lecture mein `if / else` use nahi hoga. Hum conditions ka sirf **result (`True` ya `False`) print** karenge. `if / else` Week 2 mein cover hoga.

---

## Lecture Roadmap

| Step | Topic | Maqsad |
| --- | --- | --- |
| 1 | `input()` function | User se data lena |
| 2 | Type Casting | Data ka type badalna |
| 3 | Strings | Text ke sath kaam karna |
| 4 | Comparison Operators | Do values ka muqabla karna |
| 5 | Logical Operators | Kayi conditions ko jorna |
| 6 | Final Practice | Sab kuch mila kar mini-projects |

---

## Diagram kaise parhein? (Pehle yeh samjhein)

Is lecture ke diagrams **data ke safar (flow)** ko dikhate hain:

```
 User type karta hai  ──►  Python usay le leta hai  ──►  Variable mein store  ──►  Output
```

| Nishan | Matlab |
| --- | --- |
| **`──►`** | Data agle step par ja raha hai |
| **Box** `┌───┐` | Yahan koi kaam (process) ho raha hai |
| **`▼`** | Neeche wale step par jao |

**Asaan rule:** Diagram ko hamesha **left se right** aur **upar se neeche** parhein.

---

## Pichli Class ka Revision

| Concept | Example |
| --- | --- |
| Variable | `name = "Ali"` |
| Data Types | `int`, `float`, `str`, `bool` |
| f-string | `print(f"Hello {name}")` |
| Arithmetic | `+`, `-`, `*`, `/`, `//`, `%`, `**` |

Ab tak hum ne variables mein values **khud likhi** thin (`age = 20`). Aaj hum seekhein ge ke **user se value kaise li jati hai**.

---

## Step 1: `input()` Function

### Masla (Problem)

Abhi tak program ki saari values **code mein fixed** hoti hain. Agar kisi aur student ka naam chahiye to code badalna parta hai. Real programs mein **user khud data enter karta hai**.

### Real life example

> Jab aap kisi website par **registration form** bharte hain to aap apna naam, email aur age khud likhte hain. Website wo data le kar aage use karti hai.

`input()` function bilkul yahi kaam karta hai.

### Pseudo Code

```text
START
  User se naam poochho
  Naam ko variable mein rakho
  "Hello" ke sath naam dikhao
END
```

### Diagram

```
┌──────────────────────┐
│ input("Enter name: ")│   ◄── Screen par sawal dikhta hai
└──────────────────────┘
          │
          ▼
  User "Ali" type karta hai aur Enter dabata hai
          │
          ▼
┌──────────────────────┐
│ name = "Ali"         │   ◄── Value variable mein store ho gayi
└──────────────────────┘
          │
          ▼
  print(f"Hello, {name}!")
```

### Python Syntax

```python
variable_name = input("Message jo user ko dikhana hai")
```

| Hissa | Matlab |
| --- | --- |
| `variable_name` | Wo variable jis mein user ki value store hogi |
| `input()` | Built-in function jo user se value leta hai |
| `"Message"` | Prompt: user ko batata hai ke kya enter karna hai |

> 💡 **Google Colab mein:** Cell run karne par code ke neeche ek **text box** aata hai. Us mein value type karein aur **Enter** dabayein.

### Example 1: Greeting

```python
name = input("Enter your name: ")
print(f"Hello, {name}!")
```

**Input:** `Ali`

**Output:**

```text
Hello, Ali!
```

### Step by step execution

1. Python screen par `Enter your name: ` dikhata hai.
2. Program **ruk jata hai** aur user ka intezar karta hai.
3. User `Ali` type karke Enter dabata hai.
4. `name` variable mein `"Ali"` store ho jata hai.
5. f-string se `Hello, Ali!` print hota hai.

### Example 2: Multiple Inputs

```python
name = input("Enter your name: ")
city = input("Enter your city: ")

print(f"{name} lives in {city}")
```

**Input:** `Sara`, `Karachi`

**Output:**

```text
Sara lives in Karachi
```

### ⚠️ Sab se Important Rule: `input()` hamesha `str` deta hai

User chahe number type kare, Python usay hamesha **text (string)** hi samajhta hai.

```python
age = input("Enter your age: ")   # User ne 20 type kiya

print(age)           # 20
print(type(age))     # <class 'str'>
```

Ab dekhein is se kya masla hota hai:

```python
age = input("Enter your age: ")   # User ne 20 type kiya
print(age + 1)
```

**Output:**

```text
TypeError: can only concatenate str (not "int") to str
```

Python `"20" + 1` nahi kar sakta, kyun ke ek **text** hai aur doosra **number**. Is ka hal agle step mein hai: **Type Casting**.

### Common Mistakes (aam ghaltiyan)

| Ghalat | Sahi | Wajah |
| --- | --- | --- |
| `Input("Name: ")` | `input("Name: ")` | Python **case-sensitive** hai, `input` chhote letters mein hai |
| `name = input(Enter name)` | `name = input("Enter name")` | Message hamesha **quotes** ke andar likhein |
| `age = input("Age: ")` phir `age + 1` | `age = int(input("Age: "))` | `input()` hamesha string deta hai |

### Practice Questions: `input()` (Students ke liye)

**Question 1: Welcome Message**

- **Scenario:** Ek hotel ke reception par computer guest ka naam le kar welcome message dikhata hai.
- **Given:** User ka input: `Sara`
- **Task:** User se naam lein aur `Welcome, Sara!` print karein (f-string use karein).
- **Expected Output:** `Welcome, Sara!`

**Question 2: Student Card**

- **Scenario:** School ke ID card system mein student ka naam aur class enter hoti hai.
- **Given:** Inputs: `Ahmed` (name), `Grade 9` (class)
- **Task:** Dono values lein aur `Ahmed is in Grade 9` print karein.
- **Expected Output:** `Ahmed is in Grade 9`

**Question 3: Favourite Subject**

- **Scenario:** Ek survey app students se unka favourite subject poochti hai.
- **Given:** Inputs: `Hina` (name), `Math` (subject)
- **Task:** Dono values lein aur `Hina's favourite subject is Math` print karein.
- **Expected Output:** `Hina's favourite subject is Math`

**Bonus Question: Think and Explain**

- **Task:** Code `age = input("Age: ")` mein user `25` type kare. `print(type(age))` ka output kya hoga? Aisa kyun?
- **Expected Answer:** `<class 'str'>`, kyun ke `input()` hamesha **string** return karta hai.

---

## Step 2: Type Casting

### Masla (Problem)

Step 1 mein humne dekha ke `input()` number ko bhi **text** bana deta hai. Isi liye us par calculation (`+`, `-`, `*`) nahi ho sakti.

### Type Casting kya hai?

**Type Casting** ka matlab hai ek **data type ko doosre data type mein badalna.**

### Real life example

> Agar aap ko kisi dabbe ke andar **likha hua number** ("5") mile aur aap ko usay calculator mein daal kar jama karna ho, to pehle usay **asal number (5)** banana parta hai.

### Pseudo Code

```text
START
  User se age lo (text ke tor par)
  Age ko number mein badlo
  Age mein 1 jama karo
  Naya result dikhao
END
```

### Diagram

```
 User type karta hai: 20
          │
          ▼
┌──────────────────────┐
│ input()              │──►  "20"   (str)   ◄── text
└──────────────────────┘
          │
          ▼
┌──────────────────────┐
│ int("20")            │──►   20    (int)   ◄── ab number hai
└──────────────────────┘
          │
          ▼
   20 + 1  =  21
```

### Casting Functions

| Function | Kaam | Example | Result |
| --- | --- | --- | --- |
| `int()` | Poora number banata hai | `int("25")` | `25` |
| `float()` | Decimal number banata hai | `float("9.5")` | `9.5` |
| `str()` | Text banata hai | `str(100)` | `"100"` |
| `bool()` | `True` / `False` banata hai | `bool(1)` | `True` |

### Example 1: Age Next Year

```python
age = int(input("Enter your age: "))
next_year_age = age + 1

print(f"Next year you will be {next_year_age}")
```

**Input:** `20`

**Output:**

```text
Next year you will be 21
```

### Step by step execution

1. `input()` user se `"20"` (string) leta hai.
2. `int("20")` usay number `20` bana deta hai.
3. `age` mein `20` (int) store hota hai.
4. `20 + 1` ka result `21` aata hai.

### Example 2: Decimal Number (`float`)

```python
price = float(input("Enter price: "))
quantity = int(input("Enter quantity: "))

total = price * quantity
print(f"Total bill: {total} PKR")
```

**Input:** `250.5`, `4`

**Output:**

```text
Total bill: 1002.0 PKR
```

### Example 3: Number ko Text banana (`str`)

```python
score = 95
message = "Your score is " + str(score)

print(message)
```

**Output:**

```text
Your score is 95
```

### `int()` ke Rules (Important)

```python
print(int(9.99))       # 9      → decimal hissa kat jata hai (round nahi hota)
print(int("15"))       # 15     → text jo number ki shakal mein ho
print(float(5))        # 5.0
print(int("12.5"))     # ❌ ValueError
print(int("abc"))      # ❌ ValueError
```

**Output (ghalat cases):**

```text
ValueError: invalid literal for int() with base 10: 'abc'
```

> 💡 Agar text number ki shakal mein nahi hai (jaise `"abc"`) to `int()` **error** deta hai. Error handling hum Week 4 mein seekhein ge.

### `bool()` ke Rules

| Value | `bool()` ka result |
| --- | --- |
| `0` | `False` |
| `""` (khali string) | `False` |
| Koi bhi **non-zero** number (`1`, `-5`, `100`) | `True` |
| Koi bhi **non-empty** string (`"Hi"`, `"0"`) | `True` |

```python
print(bool(0))        # False
print(bool(25))       # True
print(bool(""))       # False
print(bool("Hello"))  # True
```

### Common Mistakes (aam ghaltiyan)

| Ghalat | Sahi | Wajah |
| --- | --- | --- |
| `age = input("Age: ")` phir `age + 1` | `age = int(input("Age: "))` | Calculation se pehle casting zaroori hai |
| `price = int(input("Price: "))` (jab user `250.5` likhe) | `price = float(input("Price: "))` | Decimal wali value ke liye `float()` use karein |
| `"Age: " + 20` | `"Age: " + str(20)` | String ke sath number jorne ke liye `str()` ya f-string use karein |

### Practice Questions: Type Casting (Students ke liye)

**Question 1: Age Next Year**

- **Scenario:** Birthday app user ki age leti hai aur batati hai ke agle saal uski age kitni hogi.
- **Given:** User ka input: `20`
- **Task:** Age lein, `int` mein badlein aur `Next year you will be 21` print karein.
- **Expected Output:** `Next year you will be 21`

**Question 2: Shop Bill**

- **Scenario:** Ek shop mein cashier item ki price aur quantity enter karta hai.
- **Given:** Inputs: `250.5` (price), `4` (quantity)
- **Task:** Total bill nikal kar `Total bill: 1002.0 PKR` print karein.
- **Expected Output:** `Total bill: 1002.0 PKR`

**Question 3: Average Marks**

- **Scenario:** Teacher teen subjects ke marks enter karti hai aur average dekhna chahti hai.
- **Given:** Inputs: `70`, `80`, `90`
- **Task:** Teeno marks lein, average nikalein aur `Average marks: 80.0` print karein.
- **Expected Output:** `Average marks: 80.0`

**Question 4: Rectangle Area**

- **Scenario:** Ek carpenter table ka area maloom karna chahta hai.
- **Given:** Inputs: `12` (length), `5` (width)
- **Task:** Area nikal kar `Area: 60` print karein.
- **Expected Output:** `Area: 60`

**Question 5: Predict the Output (Bina run kiye batayein)**

```python
print(int("15") + 5)
print(str(15) + "5")
print(int(9.99))
print(bool(""))
print(float("3"))
```

- **Expected Output:**

```text
20
155
9
False
3.0
```

**Bonus Question: Think and Explain**

- **Task:** `int("hello")` run karne par kya hoga aur kyun?
- **Expected Answer:** `ValueError` aayega, kyun ke `"hello"` number ki shakal mein nahi hai.

---

## Step 3: Strings

### String kya hoti hai?

**String** text (alfaaz, jumle, characters) ko kehte hain, jo hamesha **quotes** (`" "` ya `' '`) ke andar likha jata hai.

### Real life example

> Aap ka **naam**, **email**, **address**, **WhatsApp message** sab strings hain.

### 3.1 String Banana aur Jorna (Concatenation)

```python
first_name = "Ali"
last_name = "Khan"

full_name = first_name + " " + last_name
print(full_name)
```

**Output:**

```text
Ali Khan
```

### 3.2 String ko Dohrana (Repetition)

```python
print("-" * 20)
print("Python " * 3)
```

**Output:**

```text
--------------------
Python Python Python 
```

### 3.3 `len()`: String ki Length

`len()` batata hai ke string mein kitne **characters** hain (space bhi count hota hai).

```python
text = "Python Programming"
print(len(text))
```

**Output:**

```text
18
```

> `Python` (6) + space (1) + `Programming` (11) = **18**

### 3.4 Indexing: Character Nikalna

Har character ki ek **position (index)** hoti hai jo **0** se shuru hoti hai.

```
 String:    P    y    t    h    o    n
 Index:     0    1    2    3    4    5
 Negative: -6   -5   -4   -3   -2   -1
```

```python
word = "Python"

print(word[0])     # P   → pehla character
print(word[3])     # h
print(word[-1])    # n   → aakhri character
```

### 3.5 Slicing: String ka Hissa Nikalna

**Syntax:** `string[start : end]` (**start** shamil hai, **end** shamil nahi)

```python
text = "Python Programming"

print(text[0:6])    # Python
print(text[7:])     # Programming
print(text[:6])     # Python
print(text[::-1])   # gnimmargorP nohtyP   → ulta (reverse)
```

### Diagram: Slicing `word[1:4]`

```
 String:    P    y    t    h    o    n
 Index:     0    1    2    3    4    5
                 └────────┘
              index 1 se 3 tak  (4 shamil nahi)
 Result:         "yth"
```

### 3.6 Useful String Methods

**Method** ek built-in function hota hai jo string ke sath `.` laga kar use karte hain.

| Method | Kaam | Example | Result |
| --- | --- | --- | --- |
| `.upper()` | Saare letters **bare** | `"hello".upper()` | `"HELLO"` |
| `.lower()` | Saare letters **chhote** | `"HELLO".lower()` | `"hello"` |
| `.title()` | Har lafz ka pehla letter bara | `"ali khan".title()` | `"Ali Khan"` |
| `.strip()` | Shuru aur aakhir ki **extra spaces** hatata hai | `"  hi  ".strip()` | `"hi"` |
| `.replace(old, new)` | Text badalta hai | `"I like Java".replace("Java", "Python")` | `"I like Python"` |
| `.count(x)` | Kitni baar aaya | `"banana".count("a")` | `3` |
| `.find(x)` | Pehli position batata hai (na mile to `-1`) | `"Python".find("t")` | `2` |
| `.startswith(x)` | Kya string `x` se shuru hoti hai? | `"Python".startswith("Py")` | `True` |

### Example: Data Cleaning (Real Life)

User aksar email mein extra spaces ya bare letters likh deta hai. Hum usay saaf karte hain:

```python
email = "  ALI@Gmail.COM  "

clean_email = email.strip().lower()
print(clean_email)
```

**Output:**

```text
ali@gmail.com
```

### Step by step execution

1. `email.strip()` shuru aur aakhir ki spaces hata deta hai: `"ALI@Gmail.COM"`
2. `.lower()` saare letters chhote kar deta hai: `"ali@gmail.com"`

### 3.7 Strings Immutable hoti hain

String ke kisi character ko **seedha badla nahi ja sakta.**

```python
name = "Ali"
name[0] = "S"
```

**Output:**

```text
TypeError: 'str' object does not support item assignment
```

**Hal:** Nayi string banayein.

```python
name = "Ali"
name = "S" + name[1:]
print(name)     # Sli
```

### Common Mistakes (aam ghaltiyan)

| Ghalat | Sahi | Wajah |
| --- | --- | --- |
| `"Hello" + 5` | `"Hello" + str(5)` | String ke sath number seedha nahi jur sakta |
| `word[6]` (jab `len = 6`) | `word[5]` | Index hamesha `0` se `len - 1` tak hota hai |
| `name.upper` | `name.upper()` | Method ke baad **brackets** zaroori hain |
| `text.upper()` aur umeed ke `text` badal gaya | `text = text.upper()` | Methods **nayi string** return karte hain, purani wahi rehti hai |

### Practice Questions: Strings (Students ke liye)

**Question 1: Name Formatter**

- **Scenario:** Ek form mein user ne apna naam chhote letters mein likha hai. Usay sahi format mein dikhana hai.
- **Given:** `name = "ayesha khan"`
- **Task:** Naam ko har lafz ke pehle bare letter ke sath print karein.
- **Expected Output:** `Ayesha Khan`

**Question 2: Email Cleaner**

- **Scenario:** Login form mein user ne email ke aage peeche spaces aur bare letters likh diye hain.
- **Given:** `email = "  ALI@GMAIL.COM  "`
- **Task:** Spaces hatayein aur chhote letters mein email print karein.
- **Expected Output:** `ali@gmail.com`

**Question 3: Password Length**

- **Scenario:** Ek app password ki length dikhati hai.
- **Given:** `password = "Secret123"`
- **Task:** Password ki length nikal kar `Password length: 9` print karein.
- **Expected Output:** `Password length: 9`

**Question 4: Word Replacement**

- **Scenario:** Ek teacher ne sentence mein ek lafz badalna hai.
- **Given:** `sentence = "I like Java"`
- **Task:** `Java` ko `Python` se badal kar print karein.
- **Expected Output:** `I like Python`

**Question 5: Letter Counter**

- **Scenario:** Ek word game mein kisi letter ki tadaad nikalni hai.
- **Given:** `word = "programming"`
- **Task:** Letter `m` kitni baar aaya, ye `m appears 2 times` ke format mein print karein.
- **Expected Output:** `m appears 2 times`

**Question 6: Predict the Output (Bina run kiye batayein)**

```python
s = "Python"
print(s[0])
print(s[-1])
print(s[1:4])
print(len(s))
```

- **Expected Output:**

```text
P
n
yth
6
```

**Bonus Question: Think and Explain**

- **Task:** `name = "Ali"` ke baad `name[0] = "S"` likhne par kya hoga aur kyun?
- **Expected Answer:** `TypeError` aayega, kyun ke strings **immutable** hoti hain.

---

## Step 4: Comparison Operators

### Comparison kya hai?

Do values ka **muqabla (comparison)** karna. Is ka result hamesha **`True` ya `False`** hota hai.

### Real life example

> Kya aap ki age 18 ya us se zyada hai? **Haan (True)** ya **Naa (False)**.

### Comparison Operators ki List

| Operator | Matlab | Example | Result |
| --- | --- | --- | --- |
| `==` | Barabar hai? | `5 == 5` | `True` |
| `!=` | Barabar **nahi** hai? | `5 != 3` | `True` |
| `>` | Se bara hai? | `7 > 10` | `False` |
| `<` | Se chhota hai? | `7 < 10` | `True` |
| `>=` | Bara **ya** barabar? | `10 >= 10` | `True` |
| `<=` | Chhota **ya** barabar? | `8 <= 5` | `False` |

### Pseudo Code

```text
START
  marks ki value lo
  Check karo: kya marks >= 50 hain?
  Result (True / False) dikhao
END
```

### Diagram

```
┌───────────────┐
│ marks >= 50 ? │
└───────────────┘
        │
        ▼
 marks = 70  →  70 >= 50  →  True
 marks = 40  →  40 >= 50  →  False
```

### Example 1: Numbers

```python
marks = 70

print(marks >= 50)    # True
print(marks == 100)   # False
print(marks != 70)    # False
```

**Output:**

```text
True
False
False
```

### Example 2: Strings ka Comparison

```python
print("apple" == "apple")    # True
print("Python" == "python")  # False  → capital aur small letters alag hote hain
```

### Example 3: `input()` ke sath

```python
age = int(input("Enter your age: "))

print(age >= 18)
```

**Input:** `16`

**Output:**

```text
False
```

> 💡 `int()` lagana zaroori hai, warna string ka number ke sath muqabla error dega.

### `=` aur `==` mein Farq (Bohat Important)

| Operator | Kaam | Example |
| --- | --- | --- |
| `=` | Value **store** karta hai (Assignment) | `age = 20` |
| `==` | Value ka **muqabla** karta hai (Comparison) | `age == 20` |

### Common Mistakes (aam ghaltiyan)

| Ghalat | Sahi | Wajah |
| --- | --- | --- |
| `print(age = 18)` | `print(age == 18)` | `=` muqabla nahi karta |
| `5 => 3` | `5 >= 3` | Sahi order `>=` hai, `=>` nahi |
| `"5" == 5` → `False` | `int("5") == 5` → `True` | String aur number alag types hain |

### Practice Questions: Comparison (Students ke liye)

**Question 1: Pass Check**

- **Scenario:** Ek result system check karta hai ke student ke marks pass hone ke liye kafi hain ya nahi (pass marks 50).
- **Given:** `marks = 45`
- **Task:** `marks >= 50` ka result print karein.
- **Expected Output:** `False`

**Question 2: Password Match**

- **Scenario:** Login system user ka dala hua password sahi password se match karta hai.
- **Given:** `correct_password = "abc123"`, `entered_password = "abc123"`
- **Task:** Dono ka muqabla (`==`) kar ke result print karein.
- **Expected Output:** `True`

**Question 3: Age Check (input ke sath)**

- **Scenario:** Ek website check karti hai ke user adult hai ya nahi.
- **Given:** User ka input: `18`
- **Task:** Age lein (`int`), `age >= 18` ka result print karein.
- **Expected Output:** `True`

**Question 4: Budget Check**

- **Scenario:** Ek customer ka budget 1200 rupay hai aur jootay ki price 1500 hai.
- **Given:** `price = 1500`, `budget = 1200`
- **Task:** Check karein ke kya `price <= budget` hai aur result print karein.
- **Expected Output:** `False`

**Question 5: Predict the Output (Bina run kiye batayein)**

```python
print(10 == 10.0)
print("a" == "A")
print(5 != 5)
print(7 > 3)
print(3 >= 3)
```

- **Expected Output:**

```text
True
False
False
True
True
```

**Bonus Question: Think and Explain**

- **Task:** `"Python" == "python"` ka result kya hoga aur kyun?
- **Expected Answer:** `False`, kyun ke Python strings mein **capital aur small letters ko alag** samajhta hai.

---

## Step 5: Logical Operators

### Masla (Problem)

Kabhi kabhi hamein **ek se zyada conditions** ko ek sath check karna hota hai.

### Real life example

> ATM se paise nikalne ke liye aap ke paas **card hona chahiye AUR PIN bhi sahi hona chahiye.** Dono mein se ek bhi ghalat ho to paise nahi milte.

Aisi surat mein hum **Logical Operators** use karte hain.

### Logical Operators ki List

| Operator | Matlab | Kab `True` hota hai |
| --- | --- | --- |
| `and` | **Aur** | **Dono** conditions `True` hon |
| `or` | **Ya** | **Kam az kam ek** condition `True` ho |
| `not` | **Ulta** | `True` ko `False` aur `False` ko `True` kar deta hai |

### Truth Tables

**`and` Table:**

| A | B | A `and` B |
| --- | --- | --- |
| True | True | **True** |
| True | False | False |
| False | True | False |
| False | False | False |

**`or` Table:**

| A | B | A `or` B |
| --- | --- | --- |
| True | True | True |
| True | False | True |
| False | True | True |
| False | False | **False** |

**`not` Table:**

| A | `not` A |
| --- | --- |
| True | False |
| False | True |

### Pseudo Code

```text
START
  card ki value lo (True / False)
  pin ki value lo (True / False)
  Check karo: card sahi AND pin sahi?
  Result dikhao
END
```

### Diagram: `and` Operator

```
┌──────────────┐     ┌──────────────┐
│ Condition 1  │ and │ Condition 2  │
└──────────────┘     └──────────────┘
       │                    │
       └─────────┬──────────┘
                 ▼
   Dono True?  ──►  True
   Koi ek False?  ──►  False
```

### Example 1: `and`

```python
age = 20
has_cnic = True

print(age >= 18 and has_cnic)
```

**Output:**

```text
True
```

### Step by step execution

| Step | Condition | Result |
| --- | --- | --- |
| 1 | `age >= 18` → `20 >= 18` | `True` |
| 2 | `has_cnic` | `True` |
| 3 | `True and True` | **`True`** |

### Example 2: `and` (ek condition ghalat)

```python
age = 16
has_cnic = True

print(age >= 18 and has_cnic)
```

**Output:**

```text
False
```

| Step | Condition | Result |
| --- | --- | --- |
| 1 | `age >= 18` → `16 >= 18` | `False` |
| 2 | `has_cnic` | `True` |
| 3 | `False and True` | **`False`** |

### Example 3: `or`

```python
day = "Sunday"

is_weekend = day == "Saturday" or day == "Sunday"
print(is_weekend)
```

**Output:**

```text
True
```

**Explanation:** `day == "Saturday"` `False` hai, lekin `day == "Sunday"` `True` hai. `or` mein ek bhi `True` ho to result `True` hota hai.

### Example 4: `not`

```python
is_raining = False

print(not is_raining)
```

**Output:**

```text
True
```

### Operators ka Order

Python pehle **comparison**, phir **not**, phir **and**, aur aakhir mein **or** check karta hai.

```python
print(5 > 3 or 2 > 4 and 1 > 5)
```

Pehle `2 > 4 and 1 > 5` → `False and False` → `False`, phir `5 > 3 or False` → `True or False` → **`True`**.

> 💡 Confusion se bachne ke liye **brackets `( )`** use karein: `(5 > 3) or ((2 > 4) and (1 > 5))`

### Common Mistakes (aam ghaltiyan)

| Ghalat | Sahi | Wajah |
| --- | --- | --- |
| `age >= 18 && has_cnic` | `age >= 18 and has_cnic` | Python mein `&&` nahi, `and` likhte hain |
| `a > 5 or < 10` | `a > 5 or a < 10` | Har condition **mukammal** likhni parti hai |
| `marks > 50 and < 100` | `marks > 50 and marks < 100` | Variable dobara likhna zaroori hai |
| `True and false` | `True and False` | `True` aur `False` ka pehla letter **capital** hota hai |

### Practice Questions: Logical Operators (Students ke liye)

**Question 1: ATM Access**

- **Scenario:** ATM sirf tab chalta hai jab card maujood ho aur PIN sahi ho.
- **Given:** `has_card = True`, `pin_correct = False`
- **Task:** `has_card and pin_correct` ka result print karein.
- **Expected Output:** `False`

**Question 2: Weekend Check**

- **Scenario:** Ek app check karti hai ke aaj weekend hai ya nahi (Saturday ya Sunday).
- **Given:** `day = "Sunday"`
- **Task:** `day == "Saturday" or day == "Sunday"` ka result print karein.
- **Expected Output:** `True`

**Question 3: Scholarship Eligibility**

- **Scenario:** Scholarship ke liye marks kam az kam 80 aur attendance kam az kam 75% honi chahiye.
- **Given:** `marks = 85`, `attendance = 90`
- **Task:** `marks >= 80 and attendance >= 75` ka result print karein.
- **Expected Output:** `True`

**Question 4: Umbrella Reminder**

- **Scenario:** Ek app bata deti hai ke chhatri ki zaroorat **nahi** hai jab baarish na ho rahi ho.
- **Given:** `is_raining = True`
- **Task:** `not is_raining` ka result print karein.
- **Expected Output:** `False`

**Question 5: Loan Eligibility**

- **Scenario:** Bank loan ke liye salary kam az kam 50,000 aur age kam az kam 21 honi chahiye.
- **Given:** `salary = 60000`, `age = 28`
- **Task:** `salary >= 50000 and age >= 21` ka result print karein.
- **Expected Output:** `True`

**Question 6: Predict the Output (Bina run kiye batayein)**

```python
print(True and False)
print(True or False)
print(not True)
print(5 > 3 and 2 > 4)
print(5 > 3 or 2 > 4)
```

- **Expected Output:**

```text
False
True
False
False
True
```

---

## Step 6: Final Problem Questions (Mini Projects)

Ab hum aaj ki saari cheezein (`input`, casting, strings, comparison, logical operators) mila kar use karein ge.

**Problem 1: Simple Calculator (Project 1)**

- **Scenario:** Ek shopkeeper ko chhota sa calculator chahiye jo do numbers ke operations dikha sake.
- **Given:** Inputs: `20` (first number), `6` (second number)
- **Task:** Dono numbers `int` mein lein aur neeche diye format mein print karein (division **2 decimal places** tak).
- **Expected Output:**

```text
Addition: 26
Subtraction: 14
Multiplication: 120
Division: 3.33
Remainder: 2
```

**Problem 2: Student Bio Data**

- **Scenario:** College ke admission form mein student ka naam, age aur city li jati hai.
- **Given:** Inputs: `Hina` (name), `19` (age), `Karachi` (city)
- **Task:** Teeno values lein aur do lines print karein: ek mein bio, doosri mein 5 saal baad ki age.
- **Expected Output:**

```text
Hina is 19 years old and lives in Karachi.
Age after 5 years: 24
```

**Problem 3: Bill Splitter**

- **Scenario:** Dost restaurant mein khana kha kar bill barabar taqseem karna chahte hain.
- **Given:** Inputs: `4500` (total bill), `4` (number of people)
- **Task:** Har shakhs ka hissa **2 decimal places** ke sath print karein.
- **Expected Output:** `Each person pays: 1125.00 PKR`

**Problem 4: Username Generator**

- **Scenario:** Ek website naye user ke liye automatic username banati hai.
- **Given:** Inputs: `Ayesha` (first name), `Khan` (last name), `2005` (birth year)
- **Task:** Username is tarah banayein: first name (small letters) + `_` + last name (small letters) + birth year ke **aakhri 2 digits**. Hint: `str(year)[-2:]`
- **Expected Output:** `ayesha_khan05`

**Problem 5: Admission Eligibility**

- **Scenario:** Ek university mein admission ke liye age kam az kam 18 aur marks kam az kam 60 hone chahiye.
- **Given:** Inputs: `17` (age), `88` (marks)
- **Task:** Dono values lein (`int`), eligibility check karein aur result print karein.
- **Expected Output:** `Eligible: False`

**Challenge Question: Debugging (Ghalti dhundein)**

- **Scenario:** Ek student ne do numbers ka sum nikalne ka code likha, lekin `10` aur `20` dene par answer `30` ki jagah kuch aur aa raha hai.

```python
a = input("Enter first number: ")
b = input("Enter second number: ")

print("Sum:", a + b)
```

- **Task:** Output dekhein, ghalti dhundein, code theek karein aur batayein ke ghalti kyun thi.
- **Hint:** `input()` kis type ka data deta hai?
- **Expected Output (theek code ke baad):** `Sum: 30`

---

## Final Revision

| Concept | Yaad rakhein |
| --- | --- |
| `input()` | User se value leta hai, aur **hamesha `str`** return karta hai |
| `int()` | Text ko poora number banata hai |
| `float()` | Text ko decimal number banata hai |
| `str()` | Number ko text banata hai |
| `len()` | String ke characters ginta hai |
| Indexing | Position `0` se shuru hoti hai, `-1` aakhri character hai |
| Slicing | `text[start:end]`, **end shamil nahi** hota |
| String methods | `.upper()`, `.lower()`, `.title()`, `.strip()`, `.replace()`, `.count()` |
| Comparison | `==`, `!=`, `>`, `<`, `>=`, `<=`, result hamesha `True` / `False` |
| `=` vs `==` | `=` store karta hai, `==` muqabla karta hai |
| `and` | Dono `True` hon to `True` |
| `or` | Ek bhi `True` ho to `True` |
| `not` | Result ko ulta kar deta hai |

---

## Teacher Solutions (Answer Key)

### `input()` Questions

```python
# Question 1
name = input("Enter your name: ")
print(f"Welcome, {name}!")

# Question 2
name = input("Enter your name: ")
grade = input("Enter your class: ")
print(f"{name} is in {grade}")

# Question 3
name = input("Enter your name: ")
subject = input("Enter your favourite subject: ")
print(f"{name}'s favourite subject is {subject}")
```

Bonus ka answer: `<class 'str'>`.

### Type Casting Questions

```python
# Question 1
age = int(input("Enter your age: "))
print(f"Next year you will be {age + 1}")

# Question 2
price = float(input("Enter price: "))
quantity = int(input("Enter quantity: "))
total = price * quantity
print(f"Total bill: {total} PKR")

# Question 3
m1 = int(input("Enter marks 1: "))
m2 = int(input("Enter marks 2: "))
m3 = int(input("Enter marks 3: "))
average = (m1 + m2 + m3) / 3
print(f"Average marks: {average}")

# Question 4
length = int(input("Enter length: "))
width = int(input("Enter width: "))
print(f"Area: {length * width}")
```

Question 5 ka answer: `20`, `155`, `9`, `False`, `3.0`. Bonus: `ValueError`.

### String Questions

```python
# Question 1
name = "ayesha khan"
print(name.title())

# Question 2
email = "  ALI@GMAIL.COM  "
print(email.strip().lower())

# Question 3
password = "Secret123"
print(f"Password length: {len(password)}")

# Question 4
sentence = "I like Java"
print(sentence.replace("Java", "Python"))

# Question 5
word = "programming"
print(f"m appears {word.count('m')} times")
```

Question 6 ka answer: `P`, `n`, `yth`, `6`. Bonus: `TypeError`, kyun ke strings immutable hain.

### Comparison Questions

```python
# Question 1
marks = 45
print(marks >= 50)                      # False

# Question 2
correct_password = "abc123"
entered_password = "abc123"
print(correct_password == entered_password)   # True

# Question 3
age = int(input("Enter your age: "))
print(age >= 18)                        # True (input 18)

# Question 4
price = 1500
budget = 1200
print(price <= budget)                  # False
```

Question 5 ka answer: `True`, `False`, `False`, `True`, `True`. Bonus: `False`.

### Logical Operator Questions

```python
# Question 1
has_card = True
pin_correct = False
print(has_card and pin_correct)                 # False

# Question 2
day = "Sunday"
print(day == "Saturday" or day == "Sunday")     # True

# Question 3
marks = 85
attendance = 90
print(marks >= 80 and attendance >= 75)         # True

# Question 4
is_raining = True
print(not is_raining)                           # False

# Question 5
salary = 60000
age = 28
print(salary >= 50000 and age >= 21)            # True
```

Question 6 ka answer: `False`, `True`, `False`, `False`, `True`.

### Final Problems

```python
# Problem 1: Simple Calculator
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print(f"Addition: {a + b}")
print(f"Subtraction: {a - b}")
print(f"Multiplication: {a * b}")
print(f"Division: {a / b:.2f}")
print(f"Remainder: {a % b}")

# Problem 2: Student Bio Data
name = input("Enter your name: ")
age = int(input("Enter your age: "))
city = input("Enter your city: ")

print(f"{name} is {age} years old and lives in {city}.")
print(f"Age after 5 years: {age + 5}")

# Problem 3: Bill Splitter
total_bill = float(input("Enter total bill: "))
people = int(input("Enter number of people: "))

share = total_bill / people
print(f"Each person pays: {share:.2f} PKR")

# Problem 4: Username Generator
first_name = input("Enter first name: ")
last_name = input("Enter last name: ")
year = int(input("Enter birth year: "))

username = first_name.lower() + "_" + last_name.lower() + str(year)[-2:]
print(username)

# Problem 5: Admission Eligibility
age = int(input("Enter your age: "))
marks = int(input("Enter your marks: "))

eligible = age >= 18 and marks >= 60
print(f"Eligible: {eligible}")
```

### Debugging Challenge (Theek code)

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("Sum:", a + b)
```

**Wajah:** `input()` hamesha **string** deta hai, is liye `"10" + "20"` ka result `"1020"` aata hai (strings jur jati hain). `int()` se casting karne ke baad `10 + 20 = 30` aata hai.

---

## 📝 Homework

1. Saare **Step 6 (Final Problems)** Google Colab mein solve karein.
2. Notebook ko `Week01_Class02_Homework.ipynb` ke naam se save karein.
3. **Extra Task:** Ek program banayein jo user se uska naam, city aur favourite colour le kar ek **welcome card** print kare (`-` ki line `*` repetition se banayein).
4. Notebook ka link (**Viewer** access ke sath) apne instructor ke sath share karein.

---

⬅️ [Pichli Class](../Class-01/README.md) &nbsp;|&nbsp; ➡️ **Next:** Week 02 – Class 01: Conditional Statements (`if`, `elif`, `else`)