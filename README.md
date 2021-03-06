# portfolio
## CSharp  

Csharp heb ik leren gebruiken tijdens mijn richting Informatica Beheer.  

**Overloads Definiëren**  


- https://dotnetfiddle.net/RXn26T  
- https://dotnetfiddle.net/2p3lt0  

**Declareren en gebruiken van variablen**  
  

- https://dotnetfiddle.net/B0pOkm  
- https://dotnetfiddle.net/ypzI56  
- https://dotnetfiddle.net/oUiGbX  
- https://dotnetfiddle.net/IevPq4  
--> zo heb je bevoorbeeld; integer, long, ulong, char, double , etc.

**Return waardes toepassen**  
 

- https://dotnetfiddle.net/NgvLV7  
- https://dotnetfiddle.net/7Fcpfv  
- https://dotnetfiddle.net/Y6EENw  
- https://dotnetfiddle.net/Y6EENw  
- https://dotnetfiddle.net/VT0CVE   
- https://dotnetfiddle.net/ZVfqNW  --> belangrijk
      
voorbeeld van unused code na return; https://dotnetfiddle.net/8v2NKw  ; als je een regel code invoegt na een return ga je er eigenlijk voor zorgen dat die regel code onder je return niet wordt gebruikt, dus gewoon weg wordt overgeslagen. Hij begint dan na de return terug van het begin.

**code refactoren**  
 

- https://github.com/MichielVE-immalle/CookieClickerWpf  --> volledige code
--> veel methodes worden herhaald, deze code kun je dus verkorten door alles dezelfde naam te geven, NIET VERGETEN; de namen moeten dan ook in uw XAML-code worden aangepast. Dit komt doordat deze methodes eventhandlers zijn.

nl.
```
   private void Coockie_MouseEnter(object sender, MouseEventArgs e)
        {
            Coockie.Fill = new SolidColorBrush(Colors.SaddleBrown);
            Coockie.StrokeThickness = 4;
            Coockie.Stroke = new SolidColorBrush(Colors.Black);
        }


        private void Coockie_MouseLeave(object sender, MouseEventArgs e)
        {
            Coockie.Fill = new SolidColorBrush(Colors.Gray);
            Coockie.StrokeThickness = 2;
            Coockie.Stroke = new SolidColorBrush(Colors.Black);
        }

       

        private void Coockie_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            getal = getal +1;
            teller.Text = String.Format("{0}", getal);  
        }
        
```

**if/then/else**  
  
De if-opdracht test de waarde die men heeft opgegeven.
```
int eline = 16;
if (eline == 16) --> hier gaat hij na of de integer wel degelijk 16 is. als dit effectief zo is gaat hij "leuk afprinten", als het niet                                                                                                    16 is gaat hij "niet juist afprinten.
{
      Console.WriteLine("leuk");
}
else 
{
      Console.WriteLine("Niet juist");
}
```
MERK OP: Het =-teken wordt in je code aangegeven als ==.  
         wanneer je if-functie aan 2 dingen wilt laten voldoen gebruik je '&&' bv ```if(a=3 && b=3){}```  

als je een method wilt returnen, vb. de method;

```
static void Berekening(int getal1 , int Getal 2)
{
int optelling = getal1 + getal2
return optelling
}
```

Dan moet je nog een regel code afprinten in de main method om deze afteprinten;
```
 static void Main(string[] args)
 {
 Console.WriteLine(Berekening(3 , 3));
 }
```  
vervolgens druk je op F5, hij print het getal 6 af (3+3=6).

**Optellen van een variable**  
stel je hebt de variable 'i' die gelijk staat 10. Je wilt er steeds 1 bijtellen door een While-loop te gebruiken. Hiervoor gebruik je '++' nl.  
```
 for (var i = 10; i < 26; i++){}  
```
Als je de variable nu steeds met 2 wilt verhogen doe je dit als volgt;  
 
```
 for (var i = 10; i < 26; i=i+2){}
```  
**Klassen schrijven**  
  
 ```
 public class Customer
    {
        //Fields, properties, methods and events go here...
    }
 ```
 *Een klasse kan bestaan uit:*   
 - Public-methoden  die door de gebruiker van het object kunnen worden aangeroepen om taken te verrichten.  
 - Properties om een toestand van een object te verkrijgen of te wijzigen.  
 - Constructermethode  
 - Private-methoden die alleen binnen het object toegankelijk is.  
 - Private gegevens die info over het object bevatten.  
 
 *Hoe voeg je een nieuw object toe aan je klasse?*
 ```
 Customer object1 = new Customer();
 ```
 *Voorbeeld van een klasse met objecten en outputs;*
```
public class Person
    {
        // Field
        public string name;

        // Constructor that takes no arguments.
        public Person()
        {
            name = "unknown";
        }

        // Constructor that takes one argument.
        public Person(string nm)
        {
            name = nm;
        }

        // Method
        public void SetName(string newName)
        {
            name = newName;
        }
    }
    class TestPerson
    {
        static void Main()
        {
            // Call the constructor that has no parameters.
            Person person1 = new Person();
            Console.WriteLine(person1.name);

            person1.SetName("John Smith");
            Console.WriteLine(person1.name);

            // Call the constructor that has one parameter.
            Person person2 = new Person("Sarah Jones");
            Console.WriteLine(person2.name);

            // Keep the console window open in debug mode.
            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
    // Output:
    // unknown
    // John Smith
    // Sarah Jones
```
**Gegevensstructuren**  
  
lijsten en *listbox*  
De *listbox* vind je bij de WPF applicatie onder*toolbox*. Dit object gebruik je om gegevens op te slaan die zijn ingetypt of al zijn meegeven in cs of XAML. Je kan daarna nog *items* toevoegen, verwijderen, opvragen of er mee rekenen.  
Items toevoegen aan je *listbox* kan via XAML-code of via cs.   
cs:  
``` 
private void button1_Click(object sender, System.EventArgs e)
{
    listBox1.Items.Add("Jan");
    listBox1.Items.Add("Suzy");
}
```
XAML:    
```
<ListBoxItem>Drake</ListBoxItem>
<ListBoxItem>Marc</ListBoxItem>

```  
Je kan ook items uit je lijst verwijderen door volgende code te gebruiken;  
```
ListBox1.Items.removeAt(0);
```  
--> Hier ga je vanaf het eerste item beginnen verwijderen. (index 0)   
**Override**  
* https://msdn.microsoft.com/nl-be/library/ebca9ah3.aspx  
 
**Handige sites om te leren programmeren**  
 

* https://teamtreehouse.com
* https://www.codecademy.com
* https://www.codeschool.com
* https://code.org/student    
* https://www.sololearn.com
* http://exercism.io
   
**ASCII-trap**    
     
   
```
public static void Main()
{
	PrintTrap(3);
}
static void PrintTrap(int aantalTreden)
{
	for(var i=1; i<= aantalTreden; i++){
		string s = new String('*', i);
		Console.WriteLine(s);
	}
		
}
```
de output:   
```  
           *  
           **  
           ***  
```
**Eigen werkjes**  
  
*De virtuele vriend*  
https://dotnetfiddle.net/P3ufr3  
 
##JavaScript  
  


```
Console.Log(Line)

```   
## Windows Powershell  

commands; https://ss64.com/ps/   
**Java**  
**Javascript**
***Array methods***

Arrays hebben trouwens een heleboel interessante methods, zoals:

- `push` (een element achteraan toevoegen)
- `unshift` (een element vooraan toevoegen)
- `shift` (het eerste element verwijderen)
- `pop` (het laatste element verwijderen)

Gebruik autocompletion of een web-reference (b.v. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) om te kijken welke methods er nog zijn.

Experimenteer en beantwoord volgende vragen:
- welke return-waarde returnen bovenstaande 4 methods?
- wat gebeurt er telkens met de inhoud van de array?
