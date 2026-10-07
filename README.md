```csharp
int x = 17 / 5;
int y = 17 % 5;
Console.WriteLine($"{x}, {y}");

int a1 = 5;
int res1 = ++a1 * 2;
Console.WriteLine($"{res1} ({a1})");

int a2 = 5;
int res2 = a2++ * 2;
Console.WriteLine($"{res2} ({a2})");

int divInt = 7 / 2;
double divDouble = 7.0 / 2;
Console.WriteLine($"{divInt}, {divDouble}");

int remNegative = -15 % 4;
Console.WriteLine(remNegative);

int x2 = 10;
x2 = x2++ + ++x2;
Console.WriteLine(x2);

try { int max = int.MaxValue; int res = checked(max + 1); }
catch (OverflowException ex) { Console.WriteLine(ex.GetType().Name); }

int maxUnchecked = int.MaxValue;
int resUnchecked = unchecked(maxUnchecked + 1);
Console.WriteLine(resUnchecked);

double inf = 1.0 / 0.0;
double nan = 0.0 / 0.0;
Console.WriteLine($"{inf}, {nan}");

int a = 8, b = 3;
int c = a - b * 2 + a / b;
Console.WriteLine(c);

---
﻿using System;

bool comp1 = 5 > 3;
bool comp2 = 5 >= 5;
Console.WriteLine($"{comp1}, {comp2}");

bool strEqual = "hello" == "hello";
Console.WriteLine(strEqual);

bool nanEqual = double.IsNaN == double.IsNaN;
Console.WriteLine(nanEqual);

object objA = new int[] { 1 };
object objB = new int[] { 1 };
bool objEqual = objA == objB;
Console.WriteLine(objEqual);

bool doubleEqual = 10 != 10.0;
Console.WriteLine(doubleEqual);

bool nullComp = null == null;
Console.WriteLine(nullComp);

bool exprComp = (3 < 5) == (10 >= 20);
Console.WriteLine(exprComp);

bool resAnd = 4 <= 4 && 5 > 2;
Console.WriteLine(resAnd);

char Char = 'b';
bool charComp = Char > 'a';
Console.WriteLine(charComp);

bool zeroComp = -0.0 == 0.0;
Console.WriteLine(zeroComp);

---
﻿using System;

bool Foo() => true;

bool logic1 = !true || false && true;
Console.WriteLine(logic1);

bool logic2 = false && Foo();
Console.WriteLine(logic2);

bool logic3 = false & Foo();
Console.WriteLine(logic3);

bool logic4 = true ^ false ^ true;
Console.WriteLine(logic4);

bool logic5 = !(5 > 2 || 3 < 1);
Console.WriteLine(logic5);

bool a6 = true, b6 = false;
bool logic6 = a6 && !b6 || b6 && !a6;
Console.WriteLine(logic6);

int x7 = 5;
bool logic7 = true || (x7 / 0 == 1);
Console.WriteLine(logic7);

bool logic8 = false & (10 / 1 == 1);
Console.WriteLine(logic8);

bool A = true, B = false;
bool deMorgan1 = !(A && B) == (!A || !B);
Console.WriteLine(deMorgan1);

bool deMorgan2 = !(A || B) == (!A && !B);
Console.WriteLine(deMorgan2);

---
﻿using System;

int bitAnd = 5 & 3;
Console.WriteLine(bitAnd);

int bitOr = 5 | 3;
Console.WriteLine(bitOr);

int bitXor = 5 ^ 3;
Console.WriteLine(bitXor);

int bitNot = ~0;
Console.WriteLine(bitNot);

int bitShift = 1 << 4;
Console.WriteLine(bitShift);

int bitShiftRight = 40 >> 2;
Console.WriteLine(bitShiftRight);

int n37 = 15;
bool hasBit3 = (n37 & (1 << 3)) != 0;
Console.WriteLine(hasBit3);

int n38 = 0;
n38 |= (1 << 2);
Console.WriteLine(n38);

int n39 = 16;
n39 &= ~(1 << 4);
Console.WriteLine(n39);

int bitShiftNegative = (-16) >> 2;
Console.WriteLine(bitShiftNegative);

---
﻿using System;

int x1 = 5;
x1 += 5;
Console.WriteLine(x1);

int a2 = 10;
a2 *= 2 + 3;
Console.WriteLine(a2);

int x3 = 12;
x3 >>= 2;
Console.WriteLine(x3);

int? x4 = null;
x4 ??= 42;
Console.WriteLine(x4);

string str = null;
str ??= "default";
str ??= "custom";
Console.WriteLine(str);

byte b6 = 1;
b6 += 2;
Console.WriteLine(b6);

int a7 = 5, b7 = 10, c7 = 0;
c7 = a7 = b7;
Console.WriteLine(c7);

int mask = 1;
mask <<= 3;
mask |= 2;
Console.WriteLine(mask);

int x9 = 15;
x9 %= 4;
Console.WriteLine(x9);

int defInt = default(int);
string? defStr = default(string);
Console.WriteLine($"{defInt} {(defStr == null ? "null" : defStr)}");

---
﻿using System;

int score = 75;
string res1 = score >= 60 ? "Pass" : "Fail";
Console.WriteLine(res1);

int x = 5;
int y = (x > 10) ? 100 : (x > 2) ? 50 : 0;
Console.WriteLine(y);

var task3Result = true ? 10 : 15.5;
Console.WriteLine(task3Result.GetType().Name.ToLower());

string? s4 = null;
Console.WriteLine(s4?.Length);

string? s = null;
Type typeOfLength = typeof(int?);
Console.WriteLine(typeOfLength);

string? name = null;
string res6 = name ?? "Anonymous";
Console.WriteLine(res6);

string? a = null, b = "User", c = "Admin";
string res7 = a ?? b ?? c;
Console.WriteLine(res7);

int res8 = false ? (10 / 1) : 42;
Console.WriteLine(res8);
Console.WriteLine("Нет / Ошибка компиляции");

int? count = null;
int res10 = count?.GetHashCode() ?? -1;
Console.WriteLine(res10);

---
﻿using System;

object obj1 = "Hello";
bool check1 = obj1 is string;
Console.WriteLine(check1);

object obj2 = 123;
string? s2 = obj2 as string;
Console.WriteLine(s2 == null ? "null" : s2);

try
{
    object obj3 = 123;
    string s3 = (string)obj3;
}
catch (InvalidCastException ex)
{
    Console.WriteLine(ex.GetType().Name);
}

Console.WriteLine(typeof(int) == typeof(Int32));

Console.WriteLine(sizeof(long));

Console.WriteLine(null is string);

object? x7 = null;
bool b7 = x7 is null;
Console.WriteLine(b7);

Console.WriteLine((int)3.99);

object o9 = 42;
bool blockExecuted = false;
if (o9 is int val && val > 40)
{
    blockExecuted = true;
}
Console.WriteLine(blockExecuted);

---

﻿using System;

class Program
{
    static void Main()
    {
        bool result1 = (5 > 3) && !(10 <= 2) || (4 == 5);
        Console.WriteLine($"Задание 1: {result1}");

        bool result2 = !(true && false) ^ (true || false && false);
        Console.WriteLine($"Задание 2: {result2}");

        bool result3 = ((10 & 6) == 2) && ((10 | 6) == 14);
        Console.WriteLine($"Задание 3: {result3}");

        bool result4 = (15 >> 1 == 7) && (7 << 2 == 28);
        Console.WriteLine($"Задание 4: {result4}");

        bool result5 = (8 > 5) && (3 + 2 * 4 == 11) && !(false || !true);
        Console.WriteLine($"Задание 5: {result5}");

        bool result6 = (true || false) && (false || true) ^ (true && !false);
        Console.WriteLine($"Задание 6: {result6}");

        bool result7 = (100 / 10 == 0) && (100 % 30 == 10) && !(5 - 5 != 0);
        Console.WriteLine($"Задание 7: {result7}");

        bool result8 = (4 ^ 4) == 0 && (4 ^ 0) == 4 && (0 ^ 0) == 0;
        Console.WriteLine($"Задание 8: {result8}");

        bool result9 = !(6 != 5) && ((3 >= 3) || (10 / 1 == 1));
        Console.WriteLine($"Задание 9: {result9}");

        bool result10 = (false && (10 / 1 == 1)) || (true && (20 > 15));
        Console.WriteLine($"Задание 10: {result10}");

        bool result11 = (12 & 10) > 5 || (12 | 10) < 15 && !(3 == 3);
        Console.WriteLine($"Задание 11: {result11}");

        bool result12 = ((20 >> 2) == 5) ^ ((5 << 1) == 11);
        Console.WriteLine($"Задание 12: {result12}");

        bool result13 = !(!(true || false) && (true && !false));
        Console.WriteLine($"Задание 13: {result13}");

        bool result14 = (7 > 2 ? 10 : 20) == 10 && (3 < 1 ? 5 : 15) == 15;
        Console.WriteLine($"Задание 14: {result14}");

        bool result15 = (5 & 1) == 1 && (6 & 1) == 0 && (7 & 1) == 1;
        Console.WriteLine($"Задание 15: {result15}");

        bool result16 = ((10 > 5 ? true : false) ^ (3 > 8 ? true : false)) && !false;
        Console.WriteLine($"Задание 16: {result16}");

        bool result17 = !((5 > 2 && 10 > 20) || (3 == 3 && 4 <= 4));
        Console.WriteLine($"Задание 17: {result17}");

        bool result18 = ((1 << 3) == 8) && ((16 >> 4) == 1) && ((2 << 2) == 8);
        Console.WriteLine($"Задание 18: {result18}");

        bool result19 = ((10 & 7) == 2) || ((10 | 7) == 15) ^ !(4 > 1);
        Console.WriteLine($"Задание 19: {result19}");

        bool result20 = false || true && false || true && !false;
        Console.WriteLine($"Задание 20: {result20}");

        bool result21 = (25 % 4 == 1) && (17 / 3 == 5) && (17 % 3 == 2);
        Console.WriteLine($"Задание 21: {result21}");

        bool result22 = ((5 ^ 3 ^ 3) == 5) && ((10 ^ 0) == 10);
        Console.WriteLine($"Задание 21: {result22}");

        bool result23 = (true ? (false ? 1 : 2) : (true ? 3 : 4)) == 2;
        Console.WriteLine($"Задание 23: {result23}");

        bool result24 = !(true && !(false || !false));
        Console.WriteLine($"Задание 24: {result24}");

        bool result25 = ((~0 == -1) && (~(-1) == 0));
        Console.WriteLine($"Задание 25: {result25}");

        bool result26 = ((8 & 4) == 0) && ((8 | 4) == 12) && ((8 ^ 4) == 12);
        Console.WriteLine($"Задание 26: {result26}");

        bool result27 = !(10 >= 10) || (5 < 3) && (2 == 2) || !(false);
        Console.WriteLine($"Задание 27: {result27}");

        bool result28 = !((15 & ~1) == 14) && ((14 | 1) == 15);
        Console.WriteLine($"Задание 28: {result28}");

        bool result29 = ((true || false) ? (false && true ? 10 : 20) : 30) == 20;
        Console.WriteLine($"Задание 29: {result29}");

        bool result30 = ((10 > 2) && (5 < 9)) ^ (!(4 >= 5) && (6 != 7));
        Console.WriteLine($"Задание 30: {result30}");

        bool result31 = (7 & 3 & 1) == 1 && (7 | 3 | 1) == 7;
        Console.WriteLine($"Задание 31: {result31}");

        bool result32 = ((10 > 5 && 3 < 1) || (8 == 8 && !(5 > 10))) && (4 + 4 == 8);
        Console.WriteLine($"Задание 32: {result32}");

        bool result33 = !((!(true && false) || !(true || false)) && !false);
        Console.WriteLine($"Задание 33: {result33}");

        bool result34 = ((32 >> 3 == 4) && (4 << 3 == 32)) ^ ((15 & 7) == 7 && (15 | 7) == 15);
        Console.WriteLine($"Задание 34: {result34}");

        bool result35 = ((5 > 3 ? (2 > 1 ? true : false) : false) && !((10 > 20) || (30 < 15)));
        Console.WriteLine($"Задание 35: {result35}");
   
}

!end
