# Week 01 – Class 01

## Programming Basics, Google Colab, Variables, Data Types, f-Strings & Arithmetic Operations

---

## 📌 Table of Contents

1. [Programming Language Kya Hai?](#1-programming-language-kya-hai)
2. [Programming Language Kyun Use Karte Hain?](#2-programming-language-kyun-use-karte-hain)
3. [Python Hi Kyun?](#3-python-hi-kyun)
4. [Google Colab Kya Hai?](#4-google-colab-kya-hai)
5. [Variables](#5-variables)
6. [Data Types](#6-data-types)
7. [f-Strings (Formatted Strings)](#7-f-strings-formatted-strings)
8. [Arithmetic Operations](#8-arithmetic-operations)
9. [Practice Questions](#9-practice-questions)
10. [Key Takeaways](#10-key-takeaways)

---

## 🎯 Learning Objectives

Is class ke end tak aap ye kar sakein ge:

- Programming language kya hoti hai aur kyun use hoti hai, ye explain karna
- Google Colab mein Python code run karna
- Naming rules ke sath variables create karna aur use karna
- Python ke core data types ko identify karna
- f-strings se output ko professional tareeqe se format karna
- Arithmetic operators se calculations karna

---

## 1. Programming Language Kya Hai?

**Programming language** rules aur instructions ka ek set hai jis ke zariye hum computer se baat karte hain. Computer sirf **binary** (`0` aur `1`) samajhta hai, is liye programming language insaan ki logic aur computer ke darmiyan ek **bridge** ka kaam karti hai.

```text
Human (Aap)  →  Programming Language (Python)  →  Computer
```

### Real-Life Example

Ek **recipe** ke bare mein sochein. Recipe step-by-step instructions ka set hota hai jise chef follow karke dish banata hai. Bilkul isi tarah, program bhi step-by-step instructions ka set hota hai jise computer follow karke task complete karta hai.

| Recipe | Program |
|--------|---------|
| Ingredients | Data (Input) |
| Cooking steps | Code (Logic) |
| Tayyar dish | Output (Result) |

### Programming Languages Ki Types (Overview)

| Type | Description | Examples |
|------|-------------|----------|
| **High-Level** | Insaan ke liye parhna aur likhna aasan | Python, Java, JavaScript |
| **Low-Level** | Machine language ke qareeb, mushkil | Assembly, Machine Code |

---

## 2. Programming Language Kyun Use Karte Hain?

Programming languages ke zariye hum **tasks automate** karte hain, **problems solve** karte hain aur **software build** karte hain.

| Use Case | Example |
|----------|---------|
| **Automation** | 1,000 files ko chand seconds mein rename karna |
| **Web Development** | E-commerce jaisi websites banana |
| **Mobile Apps** | Food delivery ya ride-hailing apps |
| **Data Analysis** | Sales data analyze karke business decisions lena |
| **Artificial Intelligence** | Chatbots, recommendation systems, face recognition |
| **Game Development** | Interactive games banana |
| **Banking & Finance** | Secure online transactions process karna |

---

## 3. Python Hi Kyun?

Python dunya ki sab se popular programming languages mein se ek hai, aur pehli language ke tor par bohat behtareen hai.

- ✅ **Simple aur readable syntax** – plain English ke qareeb
- ✅ **Beginner-friendly** – seekhna aasan
- ✅ **Versatile** – web, data science, AI, automation sab mein use hoti hai
- ✅ **Bari community** – tutorials, libraries aur support ki kami nahi
- ✅ **High demand** – bari companies mein widely use hoti hai

### Aapka Pehla Program

```python
print("Hello, World!")
```

**Output:**
```text
Hello, World!
```

> 💡 `print()` ek built-in **function** hai jo screen par output display karta hai.

---

## 4. Google Colab Kya Hai?

**Google Colab** (Colaboratory) Google ka free, cloud-based platform hai jis mein aap apne **web browser** mein hi Python code likh aur run kar sakte hain. Koi installation ya setup zaroori nahi.

### Google Colab Kyun Use Karte Hain?

| Benefit | Description |
|---------|-------------|
| **No Installation** | Browser mein foran coding start karein |
| **Free** | Sirf Google account chahiye |
| **Cloud Storage** | Notebooks automatically Google Drive mein save hote hain |
| **Easy Sharing** | Google Docs ki tarah link se share karein |
| **Pre-installed Libraries** | NumPy, Pandas, Matplotlib wagera pehle se maujood |
| **Kahin Se Bhi Access** | Internet wali kisi bhi device par chalta hai |

### Google Colab Start Karne Ke Steps

1. [https://colab.research.google.com](https://colab.research.google.com) open karein
2. Apne **Google account** se sign in karein
3. **File → New notebook** par click karein
4. Notebook ka naam rakhein (masalan, `Week01_Class01.ipynb`)
5. **Code cell** mein code likhein aur **Shift + Enter** press karke run karein

### Interface Ko Samjhein

| Element | Purpose |
|---------|---------|
| **Code Cell** | Jahan Python code likh kar run karte hain |
| **Text Cell** | Jahan Markdown mein notes likhte hain |
| **▶ Run Button** | Selected cell ko execute karta hai |
| **+ Code / + Text** | Naya code ya text cell add karta hai |

### Useful Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Shift + Enter` | Cell run karo aur next cell par jao |
| `Ctrl + Enter` | Cell run karo aur usi par raho |
| `Ctrl + M B` | Neeche naya cell insert karo |
| `Ctrl + M D` | Current cell delete karo |

---

## 5. Variables

### Variable Kya Hota Hai?

**Variable** ek naam wala container hai jo computer ki memory mein **data store** karta hai. Isay ek **label lage dabbe** ki tarah samjhein: label variable ka naam hai aur dabbe ke andar ki cheez uski value.

```python
name = "Ali"
age = 20
```

```text
┌─────────────┐    ┌──────────┐
│    "Ali"    │    │    20    │
└─────────────┘    └──────────┘
     name               age
```

### Variables Kyun Use Karte Hain?

- Data ko **store** karne ke liye taake baad mein dobara use ho sakay
- **Repetition se bachne** ke liye – value ek baar likhein, kai jagah use karein
- Code ko **readable** banane ke liye – meaningful names se purpose clear hota hai
- Values ko **aasani se update** karne ke liye – sirf ek jagah change karna parta hai

### Real-Life Examples

| Real-Life Situation | Variable Example |
|---------------------|------------------|
| School ID card par student ka **naam** | `student_name = "Ayesha"` |
| Shop mein product ki **price** | `product_price = 1500` |
| Bank account ka **balance** | `account_balance = 25000` |
| Weather app par **temperature** | `temperature = 32.5` |
| Dukan **open** hai ya **closed** | `is_open = True` |

### Example: Shopping Scenario

```python
item_name = "Wireless Mouse"
item_price = 1200
quantity = 3

total_cost = item_price * quantity

print("Item:", item_name)
print("Total Cost:", total_cost)
```

**Output:**
```text
Item: Wireless Mouse
Total Cost: 3600
```

> 💡 Agar price change ho jaye to sirf `item_price` ek jagah update karna hai, baqi program khud sahi chalega.

### Variable Ko Update Karna

```python
balance = 10000
print(balance)       # 10000

balance = 8500       # Purchase ke baad value update hui
print(balance)       # 8500
```

### Variable Naming Rules

| Rule | Valid ✅ | Invalid ❌ |
|------|----------|-----------|
| **Letter** ya underscore `_` se start ho | `name`, `_count` | `1name` |
| **Letters, numbers, underscores** ho sakte hain | `user_1` | `user-1`, `user 1` |
| Python **keywords** use nahi kar sakte | `my_class` | `class`, `if`, `for` |
| Names **case-sensitive** hote hain | `Age` aur `age` alag hain | — |
| **Space** allowed nahi | `first_name` | `first name` |

### Naming Best Practices

- **Meaningful names** rakhein: `tp` ki jagah `total_price`
- Multiple words ke liye **snake_case** use karein: `student_name`, `monthly_salary`
- Single letters sirf short loops ya math formulas mein use karein

```python
# ❌ Poor naming
x = 85000
y = 12

# ✅ Good naming
monthly_salary = 85000
months_worked = 12
```

---

## 6. Data Types

### Data Type Kya Hai?

**Data type** batata hai ke variable mein **kis qism ki value** hai aur us par kaun se operations ho sakte hain. Python value assign karte hi data type khud detect kar leta hai (isay **dynamic typing** kehte hain).

## 3. Data Types

### Data type ka matlab kya hai?

Data type batata hai ke koi value **kis qism (kind)** ki hai: text hai, number hai, ya haan/naa wala jawab. JavaScript isi se samajhti hai ke us value ke sath kya kiya ja sakta hai.

**Real life example:** Aap ke paas alag alag cheezon ke liye alag dibbe hote hain: water ke liye bottle, Rice ke liye dabba, paise ke liye wallet. Har cheez ki apni qism aur apna container hai. Isi tarah har value ki apni data type hoti hai.


### Common Data Types

| Data Type | Keyword | Description | Example | Real-Life Use |
|-----------|:-------:|-------------|---------|---------------|
| **Integer** | `int` | Poore numbers (decimal ke baghair) | `25`, `-7`, `1000` | Age, quantity, students ki tadaad |
| **Float** | `float` | Decimal wale numbers | `99.99`, `3.14` | Price, weight, temperature |
| **String** | `str` | Text, quotes ke andar | `"Python"`, `'Hello'` | Name, address, email |
| **Boolean** | `bool` | Sirf `True` ya `False` | `True`, `False` | Logged in hai? Payment hui? |
| **NoneType** | `None` | "Koi value nahi" ko represent karta hai | `None` | Khali ya abhi set na hui value |

### Examples

```python
age = 22                    # int
height = 5.8                # float
student_name = "Ahmed"      # str
is_enrolled = True          # bool
middle_name = None          # NoneType
```

### `type()` Se Data Type Check Karna

```python
print(type(age))            # <class 'int'>
print(type(height))         # <class 'float'>
print(type(student_name))   # <class 'str'>
print(type(is_enrolled))    # <class 'bool'>
print(type(middle_name))    # <class 'NoneType'>
```

### Real-Life Example: Student Profile

```python
student_name = "Fatima"       # str   → text
age = 19                      # int   → poora number
gpa = 3.75                    # float → decimal number
is_scholarship_holder = True  # bool  → haan/nahi

print(type(student_name))
print(type(age))
print(type(gpa))
print(type(is_scholarship_holder))
```

### Aur Data Types (Preview)

Ye aane wale weeks mein cover hon ge:

| Data Type | Example | Week |
|-----------|---------|:----:|
| `list` | `[10, 20, 30]` | 3 |
| `tuple` | `(10, 20, 30)` | 4 |
| `set` | `{1, 2, 3}` | 4 |
| `dict` | `{"name": "Ali", "age": 20}` | 4 |

### ⚠️ Common Mistake: String vs Number

```python
a = "10"      # str
b = 10        # int

print(a + a)  # 1010  → strings jur jati hain (concatenation)
print(b + b)  # 20    → numbers add hote hain
```

---

## 7. f-Strings (Formatted Strings)

### f-String Kya Hai?

**f-string** (formatted string literal) string ke andar **variable ki value insert karne** ka modern aur saaf tareeqa hai. Opening quote se pehle `f` lagayein aur variables ko curly braces `{}` mein likhein.

```python
name = "Sara"
age = 21

print(f"My name is {name} and I am {age} years old.")
```

**Output:**
```text
My name is Sara and I am 21 years old.
```

### f-Strings Kyun Use Karte Hain?

| Benefit | Explanation |
|---------|-------------|
| **Readable** | Final message kaisa dikhega, foran nazar aata hai |
| **Concise** | Purane formatting methods se kam code |
| **Type conversion ki zaroorat nahi** | Numbers khud text ban jate hain |
| **Expressions support** | `{}` ke andar calculations ho sakti hain |
| **Professional formatting** | Decimal places, alignment wagera control kar sakte hain |

### Comparison: f-String Ke Baghair vs Ke Sath

```python
name = "Usman"
marks = 88

# ❌ f-string ke baghair (concatenation, str() conversion zaroori)
print("Student " + name + " scored " + str(marks) + " marks.")

# ✅ f-string ke sath
print(f"Student {name} scored {marks} marks.")
```

### f-String Ke Andar Expressions

```python
price = 250
quantity = 4

print(f"Total bill: {price * quantity} PKR")
```

**Output:**
```text
Total bill: 1000 PKR
```

### Decimal Places Format Karna

Float ko **2 decimal places** mein dikhane ke liye `:.2f` use karein.

```python
average = 85.66666

print(f"Average Score: {average:.2f}")
```

**Output:**
```text
Average Score: 85.67
```

### Thousands Separator

```python
salary = 1250000

print(f"Annual Salary: {salary:,} PKR")
```

**Output:**
```text
Annual Salary: 1,250,000 PKR
```

### Real-Life Example: Invoice

```python
customer = "Hina"
product = "Laptop Bag"
unit_price = 3500
quantity = 2
total = unit_price * quantity

print(f"Customer : {customer}")
print(f"Product  : {product}")
print(f"Quantity : {quantity}")
print(f"Total    : {total:,} PKR")
```

**Output:**
```text
Customer : Hina
Product  : Laptop Bag
Quantity : 2
Total    : 7,000 PKR
```

---

## 8. Arithmetic Operations

### Arithmetic Operators Kya Hain?

**Arithmetic operators** wo symbols hain jin se numbers par **mathematical calculations** ki jati hain.

| Operator | Name | Example | Result |
|:--------:|------|---------|:------:|
| `+` | Addition | `10 + 3` | `13` |
| `-` | Subtraction | `10 - 3` | `7` |
| `*` | Multiplication | `10 * 3` | `30` |
| `/` | Division (hamesha `float` return karta hai) | `10 / 3` | `3.3333...` |
| `//` | Floor Division (sirf poora hissa) | `10 // 3` | `3` |
| `%` | Modulus (remainder) | `10 % 3` | `1` |
| `**` | Exponent (power) | `10 ** 3` | `1000` |

### Examples

```python
a = 17
b = 5

print(f"Addition:        {a + b}")     # 22
print(f"Subtraction:     {a - b}")     # 12
print(f"Multiplication:  {a * b}")     # 85
print(f"Division:        {a / b}")     # 3.4
print(f"Floor Division:  {a // b}")    # 3
print(f"Modulus:         {a % b}")     # 2
print(f"Exponent:        {a ** 2}")    # 289
```

### Har Operator Ka Real-Life Use

| Operator | Real-Life Scenario |
|:--------:|--------------------|
| `+` | Shopping cart ki items ki prices add karna |
| `-` | Withdrawal ke baad remaining balance nikalna |
| `*` | Total cost nikalna: price × quantity |
| `/` | Student ke marks ka average nikalna |
| `//` | 50 items se kitne **poore** boxes bharein ge agar har box mein 12 aate hain? → `50 // 12 = 4` |
| `%` | Packing ke baad kitni items **bach** gayi? → `50 % 12 = 2`; even/odd check mein bhi use hota hai |
| `**` | Square ka area (`side ** 2`) ya compound interest nikalna |

### Example: Packing Scenario (`//` aur `%`)

```python
total_items = 50
box_capacity = 12

full_boxes = total_items // box_capacity
remaining_items = total_items % box_capacity

print(f"Full boxes: {full_boxes}")
print(f"Remaining items: {remaining_items}")
```

**Output:**
```text
Full boxes: 4
Remaining items: 2
```

### Example: Even ya Odd Check (`%`)

```python
number = 14
print(f"Remainder when divided by 2: {number % 2}")   # 0 → Even number
```

> 💡 Agar `number % 2` ka result `0` ho to number **even** hai, warna **odd**.

### Operator Precedence (Order of Operations)

Python **PEMDAS** rule follow karta hai:

| Priority | Operator |
|:--------:|----------|
| 1 | `()` Parentheses |
| 2 | `**` Exponent |
| 3 | `*`, `/`, `//`, `%` (left se right) |
| 4 | `+`, `-` (left se right) |

```python
result1 = 10 + 5 * 2        # 20  (pehle multiplication)
result2 = (10 + 5) * 2      # 30  (pehle parentheses)

print(result1)
print(result2)
```

### Compound Assignment Operators

| Operator | Example | Matlab |
|:--------:|---------|--------|
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |

```python
wallet = 1000
wallet += 500       # Paise mile → 1500
wallet -= 200       # Kharch hue → 1300
print(f"Current balance: {wallet}")
```

---

## 9. Practice Questions

### 🟢 Section A: Basic Questions

1. Ek program likhein jo aapka **name**, **age** aur **city** variables mein store kare aur f-string se print kare.
2. `int`, `float`, `str` aur `bool` ke liye ek ek variable banayein. `type()` se har variable ka type print karein.
3. `a = 25` aur `b = 4` ke liye saare saat arithmetic operations ka result print karein.
4. Neeche diye gaye names mein se kaun se **invalid** hain? Wajah bhi likhein.
   `student_name`, `2nd_place`, `total-marks`, `_balance`, `class`, `my age`

---

### 🟡 Section B: Scenario-Based Questions

**Scenario 1: Grocery Store Bill 🛒**

Ek customer ye items khareedta hai:
- Rice: `2` bags, `1,800` PKR per bag
- Cooking Oil: `3` bottles, `650` PKR per bottle
- Sugar: `4` kg, `160` PKR per kg

Aisa program likhein jo **har item ki cost**, **grand total** calculate kare aur f-strings se ek saaf bill print kare.

---

**Scenario 2: Student Result Card 🎓**

Ek student ke marks (100 mein se): Math = `78`, Physics = `85`, Chemistry = `92`, English = `69`, Computer = `88`.

Aisa program likhein jo ye calculate aur print kare:
- Total marks
- Percentage
- Average marks (**2 decimal places** ke sath)

---

**Scenario 3: Mobile Data Usage 📱**

Ek user ka monthly data package `50` GB ka hai. Pehle `20` din mein usne `31.5` GB use kar liya.

Program se calculate karein:
- Remaining data
- **Per day** average data usage
- Baqi `10` din mein limit cross kiye baghair **per day** kitna data use kiya ja sakta hai

---

**Scenario 4: Bank Account Transactions 🏦**

Account ka starting balance `50,000` PKR hai. Compound assignment operators (`+=`, `-=`) use karke ye transactions karein:
- Salary credit hui: `+75,000`
- Rent pay kiya: `-30,000`
- Utility bills pay kiye: `-8,500`
- Freelance income mili: `+12,000`

Har transaction ke **baad** ka balance aur **final balance** f-strings aur comma formatting ke sath print karein.

---

**Scenario 5: Event Seating Arrangement 🎪**

Ek event organizer ke paas `275` guests hain. Har table par `8` guests baith sakte hain.

Program se calculate karein:
- **Poori tarah bhare** hue tables ki tadaad
- **Aakhri, adhoore bhare** table par kitne guests hon ge
- Total kitne tables chahiye (hint: agar guests bach jayein to ek extra table chahiye)

---

**Scenario 6: Temperature Converter 🌡️**

`36.6` °C ko is formula se Fahrenheit mein convert karein:

```text
F = (C × 9 / 5) + 32
```

Result is format mein print karein: `36.6°C is equal to 97.88°F` (2 decimal places tak round).

---

### 🔴 Section C: Challenge Question

**Scenario 7: Salary Slip Generator 💼**

Ek employee ki salary details:
- Basic Salary: `80,000` PKR
- House Allowance: basic salary ka `40%`
- Medical Allowance: basic salary ka `10%`
- Tax Deduction: **total (gross) salary** ka `5%`

Aisa program likhein jo ek **professional salary slip** display kare, jis mein ye sab ho:
- Employee name
- Basic salary
- House allowance
- Medical allowance
- Gross salary
- Tax deduction
- **Net salary**

f-strings, comma separators aur 2 decimal places use karein.

---

### 🧠 Quick Quiz (Output Predict Karein)

```python
# Q1
print(15 // 4)

# Q2
print(15 % 4)

# Q3
print(2 ** 5)

# Q4
print(type(10 / 2))

# Q5
print("5" + "3")

# Q6
x = 10
x += 5
x *= 2
print(x)
```

<details>
<summary>👉 Answers dekhne ke liye click karein</summary>

| Question | Output | Explanation |
|:--------:|:------:|-------------|
| Q1 | `3` | Floor division |
| Q2 | `3` | 15 ÷ 4 ka remainder |
| Q3 | `32` | 2 ki power 5 |
| Q4 | `<class 'float'>` | `/` operator hamesha float deta hai |
| Q5 | `53` | Strings add nahi hotin, jur jati hain |
| Q6 | `30` | (10 + 5) = 15, phir 15 × 2 = 30 |

</details>

---

## 10. Key Takeaways

- **Programming language** ke zariye hum computer ko instructions dete hain.
- **Python** simple, powerful aur beginner-friendly hai.
- **Google Colab** mein bina kisi setup ke browser mein coding ho sakti hai.
- **Variable** data store karta hai aur uska **meaningful naam** `snake_case` mein hona chahiye.
- Common **data types**: `int`, `float`, `str`, `bool`, `NoneType`. Check karne ke liye `type()` use karein.
- **f-strings** (`f"..."`) output ko saaf aur professional tareeqe se format karti hain.
- **Arithmetic operators**: `+`, `-`, `*`, `/`, `//`, `%`, `**` — aur order of operations ke liye **PEMDAS** yaad rakhein.

---

## 📝 Homework

1. **Section B** aur **Section C** ke saare practice questions Google Colab mein solve karein.
2. Notebook ko `Week01_Class01_Homework.ipynb` ke naam se save karein.
3. Notebook ka link (**Viewer** access ke sath) apne instructor ke sath share karein.

---

## 🔗 Additional Resources

- [Python Official Documentation](https://docs.python.org/3/)
- [Google Colab Welcome Notebook](https://colab.research.google.com/)
- [W3Schools Python Tutorial](https://www.w3schools.com/python/)

---

⬅️ [Main Course Par Wapas Jayein](../../README.md) &nbsp;|&nbsp; ➡️ **Next:** Week 01 – Class 02: User Input, Type Casting, Strings & Operators
