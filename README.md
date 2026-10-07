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
<img width="1901" height="996" alt="image" src="https://github.com/user-attachments/assets/b7b45223-cf02-41af-a5fb-cc1fc2d4c619" />


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
