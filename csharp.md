# Základy C#

## Základní šablona konzolové aplikace

```csharp
namespace ConsoleApp
{
    using System;
  
    internal class Program
    {
        static void Main(string[] args)
        {
        }
    }
}
```

## Proměné

Proměnou se, zjednodušeně řečeno, myslí nějaký znak, který může nabývat různých hodnot. Může to být například barva vlasů, vzdělání, výška, inteligence či úroveň čtenářských dovedností, zkrátka vše, k čemu můžeme přiřknout (změřit, pozorovat, odhnadnout, apod.) různé hodnoty.

```csharp
// celé číslo
int cislo = 12;

// znak
char znak = 'a';

// textový řetězec
string text = "Ahoj světe!";
```

## Konzole

Výpis textu na konzoli

```csharp
Console.WriteLine("Hello, World!");
```

Načtení hodnoty z klávesnice

```
string vstup = Console.ReadLine();
```

Výpis proměnných

```csharp
Console.WriteLine("Zadej své jméno");
string jmeno = Console.ReadLine();
Console.WriteLine($"Ahoj {jmeno}!");
string jmeno = Console.ReadLine();
