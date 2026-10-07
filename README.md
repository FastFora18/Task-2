## Практическая работа №2: Операторы языка C#

### | Программа 1. Операции деления и остатка
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача: Вычислите результат выражения int x = 17 / 5; int y = 17 % 5;. Ответ: x = 3, y = 2.
            int x = 17 / 5;
            int y = 17 % 5;
            Console.WriteLine("x = " + x);
            Console.WriteLine("y = " + y);
        }
    }
}
```

#### Результат выполнения:
<img width="1541" height="671" alt="1" src="https://github.com/user-attachments/assets/83f5e131-aa4f-402e-9a53-b6101be0a9ea" />



### | Программа 2. Префиксный инкремент
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2: Каково значение res после выполнения int a = 5; int res = ++a * 2;? Ответ: res = 12 (префиксный инкремент увеличивает а до 6, затем умножение).
            int a = 5;
            int res = ++a * 2;

            Console.WriteLine(\$"res = {res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1566" height="790" alt="2" src="https://github.com/user-attachments/assets/8e0a1651-3859-4a07-8431-1496637e6dea" />


### | Программа 3. Постфиксный инкремент
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //Задача 3: Каково значение res после выполнения int a = 5; int res = a++ * 2;? Ответ: res = 10(постфиксный инкремент использует исходное значение 5, затем a становится 6).

            int a = 5;
            int res = a++ * 2;

            Console.Write(\$"res = {res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="861" alt="3" src="https://github.com/user-attachments/assets/dfe46694-9c2a-4741-aee9-c1509182359e" />


### | Программа 4. Целочисленное деление и деление с плавающей точкой
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4: Чему равен результат 7 / 2 и 7.0 / 2? Ответ: 3 (целочисленное деление) и 3.5 (деление с плавающей точкой).
            int C = 7 / 2;
            decimal P = 7.0m / 2;

            Console.WriteLine(\$"Решение целочисленного делеия: {C}");
            Console.WriteLine(\$"Решение целочисленного делеия: {P}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="613" alt="4" src="https://github.com/user-attachments/assets/415c282a-783c-4bee-81fe-00e6d171ad65" />


### | Программа 5. Остаток от деления отрицательного числа
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5: Каков результат выражения -15 % 4 в C#? Ответ: -3 (знак остатка совпадает со знаком делимого).

            int q = -15 % 4;

            Console.WriteLine(\$"Результат: {q}");

        }
    }
}
```

#### Результат выполнения:
<img width="1572" height="574" alt="5" src="https://github.com/user-attachments/assets/da0a7157-50ad-4ba5-957d-861dee716443" />


### | Программа 6. Сложное выражение с инкрементами
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6: Что выведет выражение int x = 10; x = x++ + ++x;? Ответ: 22(первое слагаемое 10, после него x становится 11, префиксный инкремент делает x = 12, итог 10 + 12 = 22).

            int x = 10;
            x = x++ + ++x;
            Console.WriteLine(\$"Решение: {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1574" height="571" alt="6" src="https://github.com/user-attachments/assets/7755f878-3329-49ac-ab86-714414a9d1e9" />


### | Программа 7. Проверка переполнения (checked)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7: Что произойдет при выполнении int max = int.MaxValue; int res = checked(max + 1);? Ответ: Выбросится исключение System.OverflowException.

            int max = int.MaxValue;
            int res = checked(max + 1);

        }
    }
}
```

#### Результат выполнения:
<img width="1576" height="775" alt="7" src="https://github.com/user-attachments/assets/16b1bfd3-412e-4443-8b6e-caa1d181cf79" />


### | Программа 8. Игнорирование переполнения (unchecked)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Что произойдет при int max = int.MaxValue; int res = unchecked(max + 1);? Ответ: res = int.MinValue (произойдет переполнение без ошибки).

            int max = int.MaxValue;
            int res = unchecked(max + 1);

            Console.WriteLine(\$"Вывод {res}");

        }
    }
}
```

#### Результат выполнения:
<img width="1570" height="786" alt="8" src="https://github.com/user-attachments/assets/ea9f7480-00da-4f20-8706-71f5c9a67f62" />


### | Программа 9. Бесконечность и NaN (Not a Number)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Чему равен результат деления 1.0 / 0.0 и 0.0 / 0.0 ? Ответ : double.PositiveInfinity(Infinity) и double.NaN.

            double x = 1.0 / 0.0;
            double y = 0.0 / 0.0;

            Console.WriteLine(\$"X = {x}");
            Console.WriteLine(\$"Y = {y}");

        }
    }
}
```

#### Результат выполнения:
<img width="1558" height="794" alt="9" src="https://github.com/user-attachments/assets/5e7ee9cb-ccda-49ea-bd85-c7ab203bff76" />



### | Программа 10. Арифметический приоритет операций
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Вычислите: int a = 8; int b = 3; int c = a - b * 2 + a / b;. Ответ: 8 - 6 + 2 = 4.

            int a = 8;
            int b = 3;
            int c = a - b * 2 + a / b;

            Console.WriteLine(\$"C = {c}");

        }
    }
}
```

#### Результат выполнения:
<img width="1566" height="790" alt="10" src="https://github.com/user-attachments/assets/7010764e-eea4-479b-8216-143af316597f" />



### | Программа 11. Логические операторы сравнения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 1: Каков результат 5 > 3 и 5 >= 5? Ответ: true, true.
            bool x = 5 > 3;
            bool y = 5 >= 5;

            Console.WriteLine(\$"X = {x}");
            Console.WriteLine(\$"Y = {y}");
        }
    }
}
```

#### Результат выполнения:
<img width="1577" height="786" alt="11" src="https://github.com/user-attachments/assets/98ff3bcc-2db4-44a7-8ccd-fc9a6d53617a" />


### | Программа 12. Сравнение строк
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2: Чему равно "hello" == "hello" в C# и почему? Ответ: true, так как для типа string оператор == перегружен для посимвольного сравнения значений.
            bool x = "hello" == "hello";

            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="796" alt="12" src="https://github.com/user-attachments/assets/504c1a69-621c-4e99-8e0e-8c78ba6d7672" />


### | Программа 13. Сравнение значений NaN
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 3: Чему равно выражение double.NaN == double.NaN? Ответ: false (по стандарту IEEE 754 NaN не равен ничему, даже самому себе).
            bool x = double.NaN == double.NaN;

            Console.WriteLine(\$"{x}");

        }
    }
}
```

#### Результат выполнения:
<img width="1561" height="774" alt="13" src="https://github.com/user-attachments/assets/5bac5b91-a9e5-449c-afb7-a78edb86e8a9" />


### | Программа 14. Сравнение ссылок объектов (object)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4:  Каков результат выражения object a = new int[] { 1 }; object b = new int[] { 1 }; bool r = a == b;? Ответ: false (сравниваются ссылки на два разных объекта в куче).
            object a = new int[] { 1 };
            object b = new int[] { 1 };

            bool r = a == b;

            Console.WriteLine(\$"r = {r}");
        }
    }
}
```

#### Результат выполнения:
<img width="1558" height="789" alt="14" src="https://github.com/user-attachments/assets/48c82942-d89c-4a49-a615-3f84f2ca9f6d" />


### | Программа 15. Сравнение разных числовых типов (int и double)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5: Чему равно 10 != 10.0? Ответ: false (целое число 10 неявно приводится к 10.0, значения равны).

            bool x = 10 != 10.0;

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1570" height="779" alt="15" src="https://github.com/user-attachments/assets/fc0f7924-e2b2-4b02-bac5-93f240aae247" />



### | Программа 16. Сравнение значений null
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6: Что вернет null == null? Ответ: true.
            bool x = null == null;

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1569" height="784" alt="16" src="https://github.com/user-attachments/assets/6612c4f3-ccca-43f7-8ccc-ef4891be03f8" />


### | Программа 17. Сравнение логических выражений
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7:  Каков результат выражения (3 < 5) == (10 >= 20)? Ответ: false (true == false дает false).
            bool x = (3 < 5) == (10 >= 20);

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1561" height="782" alt="17" src="https://github.com/user-attachments/assets/2f3ebae4-1a20-4cf3-994d-8057fe74093e" />


### | Программа 18. Сравнение логических выражений
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Вычислите bool res = 4 <= 4 && 5 > 2;. Ответ: true.
            bool res = 4 <= 4 && 5 > 2;

            Console.WriteLine(\$"res = {res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1573" height="795" alt="18" src="https://github.com/user-attachments/assets/5d2e9a66-387f-474e-bd07-65f80742a97b" />



### | Программа 19. Сравнение логических выражений
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Что вернет выражение char c = 'b'; bool res = c > 'a';? Ответ: true (символы сравниваются по их числовым кодам Unicode: 98 > 97).
            char c = 'b';
            bool res = c > 'a';

            Console.WriteLine(\$"res = {res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1564" height="784" alt="19" src="https://github.com/user-attachments/assets/97dc71cb-8bbe-4fcd-a7c5-5107dffa8572" />


### | Программа 20. Сравнение логических выражений
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Сравните результат bool r = -0.0 == 0.0;. Ответ: true (ноль со знаком равен обычному нулю).
            bool r = -0.0 > 0.0;

            Console.WriteLine(\$"r = {r}");
        }
    }
}
```

#### Результат выполнения:
<img width="1570" height="775" alt="20" src="https://github.com/user-attachments/assets/828a79d3-67be-48b9-9159-4e5e8720791c" />


### | Программа 21. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 1: Вычислите: !true || false && true. Ответ: false (приоритет: ! -> && -> ||: false || false дает false).
            bool x = !true || false && true;

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1557" height="787" alt="21" src="https://github.com/user-attachments/assets/e544fef5-0f75-483d-842b-c34a42c5a9f2" />



### | Программа 22. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2: Будет ли вызван метод Foo() в false && Foo()? Ответ: Нет, благодаря короткому замыканию оператора &&.
            bool x = false && Foo();

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1561" height="786" alt="22" src="https://github.com/user-attachments/assets/b1b8aeb9-6f86-470d-814f-113b1e0d1ebd" />


### | Программа 23. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 3: Будет ли вызван метод Foo() в false & Foo()? Ответ: Да, побитовое/строгое логическое & вычисляет оба операнда.
            int x = false & Foo();

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1568" height="797" alt="23" src="https://github.com/user-attachments/assets/dd5c68bb-9399-4138-ad85-a560aaaea0b0" />


### | Программа 24. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4: Вычислите результат: true ^ false ^ true. Ответ: false (true ^ false = true, затем true ^ true = false).
            bool x = true ^ false ^ true;

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1559" height="785" alt="24" src="https://github.com/user-attachments/assets/29858993-77ac-4603-8a11-881a486eee04" />


### | Программа 25. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5:  Что вернет выражение !(5 > 2 || 3 < 1)? Ответ: false (5 > 2 истинно, внутри скобок true, отрицание дает false).
            bool x = !(5 > 2 || 3 < 1);

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1564" height="790" alt="25" src="https://github.com/user-attachments/assets/e033a7f1-eb5c-4ea5-8011-893ee5720b34" />


### | Программа 26. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6: Дано: bool a = true, b = false;. Чему равно a && !b || b && !a? Ответ: true (true && true || false && false -> true || false -> true).
            bool a = true, b = false;
            bool c = a && !b || b && !a;

            Console.WriteLine(\$"c = {c}");
        }
    }
}
```

#### Результат выполнения:
<img width="1560" height="783" alt="26" src="https://github.com/user-attachments/assets/f3f53886-ee7c-4ec0-a908-c7ca9a46d692" />



### | Программа 27. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7: Каков результат true || (x / 0 == 1) при любом целом x? Ответ: true (деление на ноль не произойдет из-за короткого замыкания ||).
            int x = 10;

            bool result = true || (x / 0 == 1);

            Console.WriteLine(\$"res = {result}");
        }
    }
}
```

#### Результат выполнения:
<img width="1556" height="784" alt="27" src="https://github.com/user-attachments/assets/8ffbcab2-e032-44a8-bb46-fc2d2260524b" />


### | Программа 28. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Каков результат false & (10 / 0 == 1)? Ответ: Выбросится исключение DivideByZeroException, так как & обязательно вычисляет правый операнд.
            bool x = false & (10 / 0 == 1);

            Console.WriteLine(\$"x = {x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1559" height="779" alt="28" src="https://github.com/user-attachments/assets/c7766db9-8903-49bc-a544-2974c2cd9f16" />


### | Программа 29. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Чему эквивалентно выражение !(A && B) по закону де Моргана? Ответ: !A || !B.
            bool A = true, B = false;
            bool Morgan = !(A && B);
            bool MorganEquivalent = !A || !B;

            Console.WriteLine(\$"{Morgan}, {MorganEquivalent}");
        }
    }
}
```

#### Результат выполнения:
<img width="1566" height="787" alt="29" src="https://github.com/user-attachments/assets/9fb79d79-243e-4608-928f-b8528a4b0c86" />


### | Программа 30. Логические операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Чему эквивалентно выражение !(A || B) по закону де Моргана? Ответ: !A && !B.
            bool A = true, B = false;
            bool Morgan = !(A || B);
            bool MorganEquivalent = !A && !B;

            Console.WriteLine(\$"{Morgan}, {MorganEquivalent}");
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="785" alt="30" src="https://github.com/user-attachments/assets/10f7bb34-4b8f-4a49-bf19-b118d517ec91" />


### | Программа 31. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 1: Чему равен результат 5 & 3 в двоичном и десятичном виде? Ответ: 0101 & 0011 = 0001 (десятичное 1).
            int x = 5 & 3;

            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1560" height="782" alt="31" src="https://github.com/user-attachments/assets/84dc443a-4568-4df7-bcd5-59aabd3ea864" />


### | Программа 32. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2: Чему равен результат 5 | 3? Ответ: 0101 | 0011 = 0111 (десятичное 7).
            int x = 5 | 3;

            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1568" height="772" alt="32" src="https://github.com/user-attachments/assets/ca3c978d-dd72-4257-a7fe-aab3db354c0c" />


### | Программа 33. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 3: Чему равен результат 5 ^ 3? Ответ: 0101 ^ 0011 = 0110 (десятичное 6).
            int x = 5 ^ 3;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1558" height="775" alt="33" src="https://github.com/user-attachments/assets/70ec68bc-38b0-4181-975f-4c38e44212d6" />




### | Программа 34. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4: Вычислите ~0 для типа int. Ответ: -1 (все биты устанавливаются в 1, что в дополнительном коде равно -1).
            int x = ~0;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1567" height="788" alt="34" src="https://github.com/user-attachments/assets/d4c6cc1e-7a5e-4094-ac12-207757a83bfb" />



### | Программа 35. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5: Чему равно 1 << 4? Ответ: 16 ( 1 × 2^4 ).
            int x = 1 << 4;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1559" height="837" alt="35" src="https://github.com/user-attachments/assets/803eef4c-f210-4e40-a7ea-dbf9f23b7eb6" />


### | Программа 36. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6: Чему равно 40 >> 2? Ответ: 10 ( 40 /  2^2 ).
            int x = 40 >> 2;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1556" height="781" alt="36" src="https://github.com/user-attachments/assets/c8e3f676-9e23-40c1-914b-bdf0b012a92a" />


### | Программа 37. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7: Как с помощью побитовой операции проверить, установлен ли третий бит числа n (маска 2^3 = 8 )? Ответ: (n & 8) != 0 или(n & (1 << 3)) != 0.
            int n = 13;
            bool x = (n & 8) != 0;
            bool y = (n & (1 << 3)) != 0;
            if (x)
            {
                Console.WriteLine("3-й бит установлен");
            }
            else
            {
                Console.WriteLine("3-й бит не установлен");
            }
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="786" alt="37" src="https://github.com/user-attachments/assets/fa0cf734-5fab-4fcc-94a3-c8f48d77dd8f" />


### | Программа 38. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Как с помощью побитовой операции установить 2 - й бит числа n в 1 ? Ответ : n = n | (1 << 2); (или n |= (1 << 2);).
            int n = 8;
            n |= (1 << 2);
            Console.WriteLine(n);
        }
    }
}
```

#### Результат выполнения:
<img width="1576" height="783" alt="38" src="https://github.com/user-attachments/assets/20b5247a-64d9-4787-9efc-dce51355fc8b" />


### | Программа 39. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Как сбросить (установить в 0) 4-й бит числа n? Ответ: n = n & ~(1 << 4); (или n &= ~(1 << 4);).
            int n = 20;
            n &= ~(1 << n);
            Console.WriteLine(\$"{n}");
        }
    }
}
```

#### Результат выполнения:
<img width="1556" height="775" alt="39" src="https://github.com/user-attachments/assets/d7aa7d7d-465a-4640-ba24-d18941f869a0" />


### | Программа 40. Побитовые операции
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Каков результат выражения (-16) >> 2 для int? Ответ: -4 (арифметический сдвиг вправо сохраняет знаковый бит 1).
            int x = (-16) >> 2;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="840" alt="40" src="https://github.com/user-attachments/assets/9258ccf0-484a-4f8b-bb81-6a6f9c682b96" />


### | Программа 41. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace program
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 1: Что делает оператор x += 5? Ответ: Эквивалентен x = x + 5 (с приведением типа при необходимости).
            int x = 10;
            x += 5;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="792" alt="41" src="https://github.com/user-attachments/assets/ab24fd73-0b26-415f-bf9d-fad764b53885" />




### | Программа 42. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2: Каково значение a после выполнения: int a = 10; a *= 2 + 3;? Ответ: 50 (правая часть вычисляется полностью перед умножением: a = a * (2 + 3)).
            int a = 10;
            a *= 2 + 3;
            Console.WriteLine(\$"{a}");
        }
    }
}
```

#### Результат выполнения:
<img width="1560" height="778" alt="42" src="https://github.com/user-attachments/assets/045e0a72-db92-41e8-9558-2f771cec548f" />


### | Программа 43. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 3: Чему равен x после int x = 12; x >>= 2;? Ответ: 3
            int x = 12;
            x >>= 2;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1570" height="804" alt="43" src="https://github.com/user-attachments/assets/0b7c4409-f576-414b-893b-7ee478769383" />




### | Программа 44. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4: Что делает оператор x ??= y? Ответ: Присваивает переменной x значение y только в том случае, если x == null.
            int? x = null;
            int y = 5;
            x = x ?? y;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1561" height="784" alt="44" src="https://github.com/user-attachments/assets/4f5a8663-cd73-40e5-862b-31d231e70a2a" />

### | Программа 45. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5: Чему будет равна строка str после: string str = null; str ??= "default"; str ??= "custom";
            string str = null;
            str = str ?? "default";
            str = str ?? "custom";
            Console.WriteLine(\$"{str}");
        }
    }
}
```

#### Результат выполнения:
<img width="1569" height="782" alt="45" src="https://github.com/user-attachments/assets/50dfe2bc-d6cd-425b-95bb-39aeba2d84a0" />



### | Программа 46. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6: Допустимо ли выражение byte b = 1; b += 2; без явного приведения? Ответ: Да, составные операторы присваивания содержат неявное сужающее приведение типа: b = (byte)(b + 2).
            byte b = 1;
            b += 2;
            Console.WriteLine(\$"{b}");
        }
    }
}
```

#### Результат выполнения:
<img width="1564" height="800" alt="46" src="https://github.com/user-attachments/assets/2ceaaf3f-416e-42b1-82e3-3c88a77b232a" />

### | Программа 47. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7: Чему равно значение c после int a = 5, b = 10, c = 0; c = a = b;? Ответ: 10 (присваивание ассоциативно справа налево).
            int a = 5, b = 10, c = 0;
            c = a = b;
            Console.WriteLine(\$"{c}, {a}");
        }
    }
}
```

#### Результат выполнения:
<img width="1574" height="788" alt="47" src="https://github.com/user-attachments/assets/79d9807b-2bb7-4bd3-846f-b28bf40c0a2c" />


### | Программа 48. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Каково значение mask после: int mask = 1; mask <<= 3; mask |= 2;? Ответ: 10 (1 << 3 = 8, затем 8 | 2 = 10).
            int mask = 1;
            mask <<= 3;
            mask |= 2;
            Console.WriteLine(\$"{mask}");
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="781" alt="48" src="https://github.com/user-attachments/assets/a7c91856-0a36-48f8-8d9c-f596c03a1ac4" />


### | Программа 49. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Чему равно x после int x = 15; x %= 4;? Ответ: 3.
            int x = 15;
            x %= 4;
            Console.WriteLine(\$"{x}");
        }
    }
}
```

#### Результат выполнения:
<img width="1575" height="784" alt="49" src="https://github.com/user-attachments/assets/13dfc2ec-bd0f-41f4-aefd-9f75f97682f8" />



### | Программа 50. Операции присваивания
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace z
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Чему равно int? count = null; int res = count?.GetHashCode() ?? -1;? Ответ: -1.
            int? count = null;
            int res = count?.GetHashCode() ?? -1;
            Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1559" height="777" alt="50" src="https://github.com/user-attachments/assets/528ae3ca-6d36-4e30-ad09-05b6acf5acd6" />



### | Программа 51. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 1: Вычислите int score = 75; string res = score >= 60 ? "Pass" : "Fail";. Ответ: "Pass".
        int score = 75;
        string res = score >= 60 ? "Pass" : "Fail";
        Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1558" height="779" alt="51" src="https://github.com/user-attachments/assets/69b66eae-b47e-43cc-93e6-5e35fc7f11ae" />



### | Программа 52. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 2 : Чему равно int x = 5; int y = (x > 10) ? 100 : (x > 2) ? 50 : 0;? Ответ: 50.
        int x = 5;
        int y = (x > 10) ? 100 : (x > 2) ? 50 : 0;
        Console.WriteLine(\$"{y}");
        }
    }
}
```

#### Результат выполнения:
<img width="1563" height="793" alt="52" src="https://github.com/user-attachments/assets/34480d32-6293-4a78-8c25-754083c0e570" />



### | Программа 53. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 3: Какой тип имеет результат выражения true ? 10 : 15.5 ? Ответ : double.
        double result = true ? 10 : 15.5;
        Console.WriteLine(\$"{result}");
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="779" alt="53" src="https://github.com/user-attachments/assets/c7d59f36-9214-4091-a9ad-daff97cfd4cd" />


### | Программа 54. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 4 : Что выведет выражение string s = null; Console.WriteLine(s?.Length);? Ответ: Ничего / null (оператор ?. предотвращает NullReferenceException).
        string s = null;
        Console.WriteLine(s?.Length);
        }
    }
}
```

#### Результат выполнения:
<img width="1566" height="787" alt="54" src="https://github.com/user-attachments/assets/640f89de-d859-4136-b12b-6dd08b308d8a" />


### | Программа 55. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 5: Какой тип имеет результат выражения s?.Length для string s? Ответ: int? (Nullable<int>).
        string s = "Сигмаплеер";
        int? lenght = s?.Length;
        Console.WriteLine(\$"{lenght}");
        }
    }
}
```

#### Результат выполнения:
<img width="1560" height="773" alt="55" src="https://github.com/user-attachments/assets/e381fe5a-bea3-485c-abd4-6fca5ddcb906" />




### | Программа 56. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 6: Вычислите: string name = null; string res = name ?? "Anonymous";. Ответ: "Anonymous".
        string name = null;
        string res = name ?? "Anonymous";
        Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="796" alt="56" src="https://github.com/user-attachments/assets/6ba8da68-3e91-4a23-b4c5-f03cb2ae7aa1" />


### | Программа 57. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 7: Вычислите: string a = null, b = "User", c = "Admin"; string res = a ?? b ?? c;. Ответ: "User".
        string a = null, b = "User", c = "Admin";
        string res = a ?? b ?? c;
        Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1564" height="796" alt="57" src="https://github.com/user-attachments/assets/abeaf63a-79e5-469c-854d-21ea317843a5" />



### | Программа 58. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 8: Что вернет выражение false ? (10 / 0) : 42 ? Ответ : 42(второй операнд не вычисляется из - за ложного условия).
        int zero = 0;
        int result = false ? (10 / zero) : 42;
        Console.WriteLine(\$"{result}");
        }
    }
}
```

#### Результат выполнения:
<img width="1558" height="788" alt="58" src="https://github.com/user-attachments/assets/282319c1-b8f7-4722-afe9-e2f76858ee8a" />




### | Программа 59. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 9: Скомпилируется ли код var x = condition ? 10 : "text";? Ответ: Нет (в классическом C#), так как у типов int и string нет неявного взаимного приведения.
        bool condition = true;
        var x = condition ? 10 : "text"; // код не скомпилируется, как дано по условию
        }
    }
}
```

#### Результат выполнения:
<img width="1566" height="787" alt="59" src="https://github.com/user-attachments/assets/5af97cb1-60dd-43bd-970e-63604f8ea95d" />



### | Программа 60. Тернарная операция
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace l
{
    internal class Program
    {
        static void Main(string[] args)
        {
        // Задача 10: Чему равно int? count = null; int res = count?.GetHashCode() ?? -1;? Ответ: -1.
        int? count = null;
        int res = count?.GetHashCode() ?? -1;
        Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1565" height="791" alt="60" src="https://github.com/user-attachments/assets/597ecc8a-384c-4766-bed2-bcacae392987" />


### | Программа 61. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 1: Что вернет выражение object obj = "Hello"; bool check = obj is string;? Ответ: true.
            object obj = "Hello";
            bool check = obj is string;
            Console.WriteLine(\$"{check}");
        }
    }
}
```

#### Результат выполнения:
<img width="1560" height="802" alt="61" src="https://github.com/user-attachments/assets/2aba875d-8d9f-4507-b7e4-45720e8f9ea3" />


### | Программа 62. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 2 : Что вернет object obj = 123; string s = obj as string;? Ответ: null (оператор as возвращает null при невозможности безопасного приведения ссылочного типа).
            object obj = 123;
            string s = obj as string;
            Console.WriteLine(s ?? "null");
        }
    }
}
```

#### Результат выполнения:
<img width="1571" height="789" alt="62" src="https://github.com/user-attachments/assets/4e91d8da-6474-4a43-b4e7-5141f144b122" />


### | Программа 63. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 3: Что произойдет при явном приведении object obj = 123; string s = (string)obj;? Ответ: Выбросится исключение System.InvalidCastException.
            object obj = 123;
            string s = (string)obj;
            Console.WriteLine(\$"{s}");
        }
    }
}
```

#### Результат выполнения:
<img width="1569" height="787" alt="63" src="https://github.com/user-attachments/assets/945f60e9-87e4-4d41-b0ce-b5b125f00b9a" />


### | Программа 64. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 4: Что вернет typeof(int) == typeof(Int32)? Ответ: true (псевдоним языка ссылается на один и тот же тип CLR).
            bool res = typeof(int) == typeof(Int32);
            Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1556" height="805" alt="64" src="https://github.com/user-attachments/assets/17a8f3c7-1cf0-4d24-ae80-a82494a46e89" />


### | Программа 65. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 5: Чему равен результат sizeof(long) в байтах? Ответ: 8.
            int res = sizeof(long);
            Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1532" height="782" alt="65" src="https://github.com/user-attachments/assets/4c7f8a3b-55c0-4af8-b80c-fb9cad8a6d84" />


### | Программа 66. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 6 : Что вернет null is string? Ответ: false (шаблон is для null всегда возвращает false, кроме шаблона is null).
            object obj = null;
            bool res = obj is string;
            Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1533" height="786" alt="66" src="https://github.com/user-attachments/assets/84c39939-f2ae-44b7-9786-7d66d164a6f7" />


### | Программа 67. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 7: Что вернет выражение object x = null; bool b = x is null;? Ответ: true.
            object x = null;
            bool b = x is null;
            Console.WriteLine(\$"{b}");
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="790" alt="67" src="https://github.com/user-attachments/assets/16f72586-987a-482a-bcbd-86f1bc152552" />



### | Программа 68. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 8: Каков результат (int)3.99? Ответ: 3 (дробная часть отсекается без округления).
            int res = (int)3.99;
            Console.WriteLine(\$"{res}");
        }
    }
}
```

#### Результат выполнения:
<img width="1541" height="788" alt="68" src="https://github.com/user-attachments/assets/716e9c6f-656d-44e0-a3b4-c5ce3bf705a4" />

### | Программа 69. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 9: Каков результат pattern matching: object o = 42; if (o is int val && val > 40) { ... } Будет ли выполнено тело блока? Ответ: Да, val получит значение 42, условие val > 40 истинно.
            object o = 42;
            if (o is int val && val > 40)
            {
                Console.WriteLine(\$"val = {val}");
            }
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="784" alt="69" src="https://github.com/user-attachments/assets/35e31166-7fc4-4385-8a1f-e0cf36d63be9" />



### | Программа 70. Операторы приведения типов (is / as)
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Задача 10: Что вернет выражение default(int) и default(string)? Ответ: 0 и null.
            Console.WriteLine(\$"{default(int)}, {default(string) ?? "null"}");
        }
    }
}
```

#### Результат выполнения:
<img width="1539" height="787" alt="70" src="https://github.com/user-attachments/assets/82adb24b-b45d-4db6-b624-be6671dce6d6" />


### | Программа 71. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(5 > 3) && !(10 <= 2) || (4 == 5)
bool result1 = (5 > 3) && !(10 <= 2) || (4 == 5);
Console.WriteLine(result1);
        }
    }
}
```

#### Результат выполнения:
<img width="1536" height="785" alt="71" src="https://github.com/user-attachments/assets/41d4f612-6a68-467e-bb2f-f4787e17bf03" />


### | Программа 72. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!(true && false) ^ (true || false && false)
           bool result2 = !(true && false) ^ (true || false && false);
Console.WriteLine(result2);
        }
    }
}
```

#### Результат выполнения:
<img width="1526" height="781" alt="72" src="https://github.com/user-attachments/assets/4daf5148-a178-4834-9f1c-2883af5fc5f9" />


### | Программа 73. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(10 & 6) == 2 && (10 | 6) == 14
           bool result3 = (10 & 6) == 2 && (10 | 6) == 14;
Console.WriteLine(result3);
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="783" alt="73" src="https://github.com/user-attachments/assets/0a938f14-8b2a-4ea9-a444-d7c563f7e92b" />




### | Программа 74. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(15 >> 1 == 7) && (7 << 2 == 28)
           bool result4 = (15 >> 1 == 7) && (7 << 2 == 28);
Console.WriteLine(result4);
        }
    }
}
```

#### Результат выполнения:
<img width="1535" height="785" alt="74" src="https://github.com/user-attachments/assets/366e5033-9c71-4e57-8942-1433ebd7e489" />


### | Программа 75. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(8 > 5) && (3 + 2 * 4 == 11) && !(false || !true)
           bool result5 = (8 > 5) && (3 + 2 * 4 == 11) && !(false || !true);
Console.WriteLine(result5);
        }
    }
}
```

#### Результат выполнения:
<img width="1530" height="785" alt="75" src="https://github.com/user-attachments/assets/cada6dce-2b29-4100-b60b-3ac477a7b6cb" />


### | Программа 76. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(true || false) && (false || true) ^ (true && !false)
           bool result6 = (true || false) && (false || true) ^ (true && !false);
Console.WriteLine(result6);
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="793" alt="76" src="https://github.com/user-attachments/assets/484c8115-f2fa-454c-a614-936950a4d27b" />


### | Программа 77. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(100 / 10 == 10) && (100 % 30 == 10) && !(5 - 5 != 0)
           bool result7 = (100 / 10 == 10) && (100 % 30 == 10) && !(5 - 5 != 0);
Console.WriteLine(result7);
        }
    }
}
```

#### Результат выполнения:
<img width="1530" height="780" alt="77" src="https://github.com/user-attachments/assets/3454cff3-ed34-40d5-83e2-bbd1bab919eb" />


### | Программа 78. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(4 ^ 4) == 0 && (4 ^ 0) == 4 && (0 ^ 0) == 0
           bool result8 = (4 ^ 4) == 0 && (4 ^ 0) == 4 && (0 ^ 0) == 0;
Console.WriteLine(result8);
        }
    }
}
```

#### Результат выполнения:
<img width="1534" height="788" alt="78" src="https://github.com/user-attachments/assets/fa1ae5ee-fb53-4f23-8c80-099960e2ebe6" />


### | Программа 79. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!(5 != 5) && ((3 >= 3) || (10 / 0 == 1))
           bool result9 = !(5 != 5) && ((3 >= 3) || (10 / 0 == 1));
Console.WriteLine(result9);
        }
    }
}
```

#### Результат выполнения:
<img width="1527" height="786" alt="79" src="https://github.com/user-attachments/assets/f7345668-cac8-4ec2-8ce6-4b546033ed0b" />


### | Программа 80. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(false && (10 / 0 == 1)) || (true && (20 > 15))
           bool result10 = (false && (10 / 0 == 1)) || (true && (20 > 15));
Console.WriteLine(result10);
        }
    }
}
```

#### Результат выполнения:
<img width="1529" height="775" alt="80" src="https://github.com/user-attachments/assets/ea8c6b7d-6cac-46c1-b35d-42e48ae033be" />


### | Программа 81. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(12 & 10) > 5 || (12 | 10) < 15 && !(3 == 3)
          bool result11 = (12 & 10) > 5 || (12 | 10) < 15 && !(3 == 3);
Console.WriteLine(result11); 
        }
    }
}
```

#### Результат выполнения:
<img width="1534" height="778" alt="81" src="https://github.com/user-attachments/assets/0c5d1410-babd-4d58-8192-cd082e88d884" />


### | Программа 82. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//((20 >> 2) == 5) ^ ((5 << 1) == 11)
          bool result12 = ((20 >> 2) == 5) ^ ((5 << 1) == 11);
Console.WriteLine(result12); 
        }
    }
}
```

#### Результат выполнения:
<img width="1523" height="808" alt="82" src="https://github.com/user-attachments/assets/7cecd1af-0cf5-4c9b-9098-7ba626854efb" />


### | Программа 83. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!(!(true || false) && (true && !false))
           bool result13 = !(!(true || false) && (true && !false));
Console.WriteLine(result13);
        }
    }
}
```

#### Результат выполнения:
<img width="1530" height="798" alt="83" src="https://github.com/user-attachments/assets/bfac77c1-fb92-4cc9-a03f-d1167271f215" />


### | Программа 84. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(7 > 2 ? 10 : 20) == 10 && (3 < 1 ? 5 : 15) == 15
           bool result14 = (7 > 2 ? 10 : 20) == 10 && (3 < 1 ? 5 : 15) == 15;
Console.WriteLine(result14);
        }
    }
}
```

#### Результат выполнения:
<img width="1516" height="790" alt="84" src="https://github.com/user-attachments/assets/1c3843ee-27b4-4b0b-8772-197e70584dae" />


### | Программа 85. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(5 & 1) == 1 && (6 & 1) == 0 && (7 & 1) == 1 (проверка на нечетность)
        bool result15 = (5 & 1) == 1 && (6 & 1) == 0 && (7 & 1) == 1;
Console.WriteLine(result15);   
        }
    }
}
```

#### Результат выполнения:
<img width="1519" height="782" alt="85" src="https://github.com/user-attachments/assets/6ebe57eb-61c3-4d8c-bd25-e582a41e947b" />



### | Программа 86. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//((10 > 5 ? true : false) ^ (3 > 8 ? true : false)) && !false
           bool result16 = ((10 > 5 ? true : false) ^ (3 > 8 ? true : false)) && !false;
Console.WriteLine(result16);
        }
    }
}
```

#### Результат выполнения:
<img width="1535" height="783" alt="86" src="https://github.com/user-attachments/assets/67844a3a-c2a2-4783-9a9f-beace81c5ea4" />


### | Программа 87. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!( (5 > 2 && 10 > 20) || (3 == 3 && 4 <= 4) )
           bool result17 = !((5 > 2 && 10 > 20) || (3 == 3 && 4 <= 4));
Console.WriteLine(result17);
        }
    }
}
```

#### Результат выполнения:
<img width="1522" height="749" alt="87" src="https://github.com/user-attachments/assets/be9609c5-9653-4641-bf13-bbab3cc41e80" />


### | Программа 88. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (1 << 3) == 8 ) && ( (16 >> 4) == 1 ) && ( (2 << 2) == 8 )
           bool result18 = ((1 << 3) == 8) && ((16 >> 4) == 1) && ((2 << 2) == 8);
Console.WriteLine(result18);
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="784" alt="88" src="https://github.com/user-attachments/assets/83369cd7-2e3e-4858-8b9f-569999b80565" />


### | Программа 89. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (10 & 7) == 2 ) || ( (10 | 7) == 15 ) ^ !(4 > 1)
          bool result19 = ((10 & 7) == 2) || ((10 | 7) == 15) ^ !(4 > 1);
Console.WriteLine(result19); 
        }
    }
}
```

#### Результат выполнения:
<img width="1522" height="783" alt="89" src="https://github.com/user-attachments/assets/76b8226c-adc5-4b9c-915a-9d76c23ac149" />


### | Программа 90. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//false || true && false || true && !false
           bool result20 = false || true && false || true && !false;
Console.WriteLine(result20);
        }
    }
}
```

#### Результат выполнения:
<img width="1525" height="787" alt="90" src="https://github.com/user-attachments/assets/3aeb89d2-46b8-4cf5-8a9b-e2ae06215dd9" />


### | Программа 91. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(25 % 4 == 1) && (17 / 3 == 5) && (17 % 3 == 2)
          bool result21 = (25 % 4 == 1) && (17 / 3 == 5) && (17 % 3 == 2);
Console.WriteLine(result21); 
        }
    }
}
```

#### Результат выполнения:
<img width="1533" height="783" alt="91" src="https://github.com/user-attachments/assets/1b60faf0-4955-4bae-b17b-c59a2d80f31c" />


### | Программа 92. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (5 ^ 3 ^ 3) == 5 ) && ( (10 ^ 0) == 10 )
        bool result22 = ((5 ^ 3 ^ 3) == 5) && ((10 ^ 0) == 10);
Console.WriteLine(result22);   
        }
    }
}
```

#### Результат выполнения:
<img width="1520" height="778" alt="92" src="https://github.com/user-attachments/assets/7eb50601-7b17-47b1-a775-a8fa8cb39247" />


### | Программа 93. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(true ? (false ? 1 : 2) : (true ? 3 : 4)) == 2
        bool result23 = (true ? (false ? 1 : 2) : (true ? 3 : 4)) == 2;
Console.WriteLine(result23);   
        }
    }
}
```

#### Результат выполнения:
<img width="1535" height="771" alt="93" src="https://github.com/user-attachments/assets/6a6f6b97-b829-495c-ab00-c340c3a7cc0c" />


### | Программа 94. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!(true && !(false || !false))
       bool result24 = !(true && !(false || !false));
Console.WriteLine(result24);    
        }
    }
}
```

#### Результат выполнения:
<img width="1531" height="787" alt="94" src="https://github.com/user-attachments/assets/1f5650ac-9e17-40ca-860a-be9c582afd35" />



### | Программа 95. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (~0 == -1) && (~(-1) == 0) )
         bool result25 = (~0 == -1) && (~(-1) == 0);
Console.WriteLine(result25);  
        }
    }
}
```

#### Результат выполнения:
<img width="1535" height="781" alt="95" src="https://github.com/user-attachments/assets/c44cf8b8-1f24-421f-8ec6-9d51682f742c" />


### | Программа 96. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (8 & 4) == 0 ) && ( (8 | 4) == 12 ) && ( (8 ^ 4) == 12 )
           bool result26 = ((8 & 4) == 0) && ((8 | 4) == 12) && ((8 ^ 4) == 12);
Console.WriteLine(result26);
        }
    }
}
```

#### Результат выполнения:
<img width="1536" height="780" alt="96" src="https://github.com/user-attachments/assets/9310f58f-7f1b-47c2-9632-b8e6eeec49b6" />


### | Программа 97. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!(10 >= 10) || (5 < 3) && (2 == 2) || !(false)
      bool result27 = !(10 >= 10) || (5 < 3) && (2 == 2) || !(false);
Console.WriteLine(result27);     
        }
    }
}
```

#### Результат выполнения:
<img width="1498" height="757" alt="97" src="https://github.com/user-attachments/assets/4fb8b5d9-cdba-437e-8cca-bdc4d0ad1cbf" />


### | Программа 98. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (15 & ~1) == 14 ) && ( (14 | 1) == 15 )
           bool result28 = ((15 & ~1) == 14) && ((14 | 1) == 15);
Console.WriteLine(result28);
        }
    }
}
```

#### Результат выполнения:
<img width="1519" height="836" alt="98" src="https://github.com/user-attachments/assets/44994c82-fa2d-4cef-8d8e-43e7afdc0924" />


### | Программа 99. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (true || false) ? (false && true ? 10 : 20) : 30 ) == 20
           bool result29 = ((true || false) ? (false && true ? 10 : 20) : 30) == 20;
Console.WriteLine(result29);
        }
    }
}
```

#### Результат выполнения:
<img width="1536" height="793" alt="99" src="https://github.com/user-attachments/assets/b30ea854-5ad2-4fa1-876c-7f13314c189c" />


### | Программа 100. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (10 > 2) && (5 < 9) ) ^ ( !(4 >= 5) && (6 != 7) )
           bool result30 = ((10 > 2) && (5 < 9)) ^ (!(4 >= 5) && (6 != 7));
Console.WriteLine(result30);
        }
    }
}
```

#### Результат выполнения:
<img width="1538" height="783" alt="100" src="https://github.com/user-attachments/assets/0af35695-eb32-4c1d-ba9b-afb7af247d8b" />


### | Программа 101. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//(7 & 3 & 1) == 1 && (7 | 3 | 1) == 7
        bool result31 = (7 & 3 & 1) == 1 && (7 | 3 | 1) == 7;
Console.WriteLine(result31);   
        }
    }
}
```

#### Результат выполнения:
<img width="1533" height="786" alt="101" src="https://github.com/user-attachments/assets/f9870122-4913-4703-b168-b55433aed653" />


### | Программа 103. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//!( (!(true && false) || !(true || false)) && !false )
           bool result33 = !((!(true && false) || !(true || false)) && !false);
Console.WriteLine(result33);
        }
    }
}
```

#### Результат выполнения:
<img width="1535" height="797" alt="103" src="https://github.com/user-attachments/assets/6af5bb38-e877-448b-9aa5-2de6408289b5" />


### | Программа 104. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (32 >> 3 == 4) && (4 << 3 == 32) ) ^ ( (15 & 7) == 7 && (15 | 7) == 15 )
          bool result34 = (((32 >> 3) == 4) && ((4 << 3) == 32)) ^ (((15 & 7) == 7) && ((15 | 7) == 15));
Console.WriteLine(result34); 
        }
    }
}
```

#### Результат выполнения:
<img width="1527" height="783" alt="104" src="https://github.com/user-attachments/assets/557e8b9a-b952-4861-8520-a096227d982b" />


### | Программа 105. Сложные логические выражения
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Cons
{
    internal class Program
    {
        static void Main(string[] args)
        {
//( (5 > 3 ? (2 > 1 ? true : false) : false) && !( (10 > 20) || (30 < 15) ) )
           bool result35 = (5 > 3 ? (2 > 1 ? true : false) : false) && !((10 > 20) || (30 < 15));
Console.WriteLine(result35);
        }
    }
}
```

#### Результат выполнения:
<img width="1532" height="788" alt="105" src="https://github.com/user-attachments/assets/112cdd15-16cf-473b-9897-df38c43660cd" />

!end
