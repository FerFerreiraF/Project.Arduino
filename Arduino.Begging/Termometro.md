# Termometro

```cpp
#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);
int ENTRADAA0 = 0, ENTRADAA1 = 0, Temp = 0;

void setup()
{
  lcd.begin(16, 2); // Set up the number of columns and rows on the LCD.
  pinMode (A0, INPUT);
  pinMode (A1, INPUT);
}

void loop()
{
  //PORTD |= B10000000;
  ENTRADAA0 = analogRead(A0);
  ENTRADAA1 = analogRead(A1);
  //PORTD &= B01111111;
  //lcd.print("A0= ");
  //lcd.print(ENTRADAA0);
  //lcd.print(" A1= ");
  //lcd.print(ENTRADAA1);
  Temp = ENTRADAA1*0.196 - 50;
  lcd.print("T = ");
  lcd.print(Temp);
  lcd.print ("C");
  delay(1000);
  lcd.clear();
}
```

