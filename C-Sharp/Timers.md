# Timers in C#

## Infinite loop with random delay

```cs
while (true)
            {
                Random random = new Random();
                int randomNumber = random.Next(1000, 3000);
                Thread.Sleep(randomNumber);
                Console.WriteLine(randomNumber);
            }
```           
