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

Načtení vstupu z klávesnice

```
string vstup = Console.ReadLine();
```

Výpis proměnných

```csharp
Console.WriteLine("Zadej své jméno");
string jmeno = Console.ReadLine();
Console.WriteLine($"Ahoj {jmeno}!");
string jmeno = Console.ReadLine();

## Podmínky

Pokud potřebujeme reagovat a větvit program podle určité situace (např. hodnota zadaná uživatelem).

### if - else

Jestliže platí podmínka v závorce, provede se kód uvnitř bloku if, v opačném případě se provede kód uvnitř bloku else

```
int cislo = int.Parse(Console.ReadLine());
if (cislo > 10)
{
    Console.WriteLine("Číslo je větší než 10");
}
else
{
    Console.WriteLine("Číslo není větší než 10.");
}
```

### if - elseif

V některých případech může rozhodování skončit více než 2 stavy.

```csharp
if (cislo > 10)
{
    Console.WriteLine("Číslo je větší než 10");
}
else if (cislo < 10)
{
    Console.WriteLine("Číslo je menší než 10.");
}
else
{
    Console.WriteLine("Číslo rovná se deset.");
}
```

Blok else je nepovinný, pokud ho nepotřebujeme, nemusíme ho uvádět.

### Vnořené podmínky

Podmínky můžeme libovolně vnořit do sebe. Pomocí krokování si můžeme ověřit, že vše funguje dle našich představ.

```csharp
Console.OutputEncoding = System.Text.Encoding.UTF8;
int hodiny = int.Parse(Console.ReadLine());

if (hodiny > 23)
{
    Console.WriteLine("Neplatný čas.");
}
else if (hodiny > 6)
{
    if (hodiny < 8)
    {
        Console.WriteLine("Dobré ráno. ");
    }
    else if (hodiny < 12)
    {
        Console.WriteLine("Dobré dopoledne.");
    }
    else if (hodiny == 12)
    {
        Console.WriteLine("Dobré poledne.");
    }
    else if (hodiny < 18)
    {
        Console.WriteLine("Dobré odpoledne.");
    }
    else if (hodiny < 22)
    {
        Console.WriteLine("Dobrý večer.");
    }
    else
    {
        Console.WriteLine("Dobrou noc.");
    }
}
else
{
    Console.WriteLine("😴😴😴");
}
```
