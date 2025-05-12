1️⃣ EqualArrays 🔍
Namespace: \_01.EqualArrays
📌 Description:
Reads two arrays of integers and compares them element by element. If all elements match, it prints `"Arrays are identical."`; otherwise, it prints `"Arrays are not identical."`.

📝 Code:

```csharp
namespace _01.EqualArrays
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[] firstArray = ReadIntArray();
            int[] secondArray = ReadIntArray();

            for (int i = 0; i < firstArray.Length; i++)
            {
                if (firstArray[i] != secondArray[i])
                {
                    Console.WriteLine("Arrays are not identical.");
                    return;
                }
            }

            Console.WriteLine("Arrays are identical.");
        }

        private static int[] ReadIntArray()
        {
            return Console.ReadLine()
                          .Split()
                          .Select(int.Parse)
                          .ToArray();
        }
    }
}
```

2️⃣ CommonElements 🎯
Namespace: \_02.CommonElements
📌 Description:
Finds and prints common elements between two arrays (first occurrence only for each match).

📝 Code:

```csharp
namespace _02.CommonElements
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[] firstArray = ReadIntArray();
            int[] secondArray = ReadIntArray();

            foreach (int firstArrayNumber in firstArray)
            {
                foreach (int secondArrayNumber in secondArray)
                {
                    if (firstArrayNumber == secondArrayNumber)
                    {
                        Console.Write($"{firstArrayNumber} ");
                        break;
                    }
                }
            }
        }

        private static int[] ReadIntArray()
        {
            return Console.ReadLine()
                          .Split()
                          .Select(int.Parse)
                          .ToArray();
        }
    }
}
```

3️⃣ CondenseArrayToNumber 🔄
Namespace: \_03.CondenseArrayToNumber
📌 Description:
Sums adjacent elements of an array until only one number remains. Outputs the final condensed result.

📝 Code:

```csharp
namespace _03.CondenseArrayToNumber
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[] numbers = ReadIntArray();

            while (numbers.Length > 1)
            {
                int[] tempArray = new int[numbers.Length - 1];
                for (int i = 0; i < tempArray.Length; i++)
                {
                    tempArray[i] = numbers[i] + numbers[i + 1];
                }

                numbers = tempArray;
            }

            Console.WriteLine(numbers[0]);
        }

        private static int[] ReadIntArray()
        {
            return Console.ReadLine()
                          .Split()
                          .Select(int.Parse)
                          .ToArray();
        }
    }
}
```

📅 Commit Progress Update:

📅 Current Progress: 415 commits
📊 Progress Bar:
████████████████████████████████████▍83.0% (415/500)

📌 Milestones:
✅ 100 commits
✅ 200 commits
✅ 300 commits
✅ 400 commits
🔲 500 commits (🎉)

🎯 Commit Progress Tracker

🚀 Goal: 500 commits in 2025
