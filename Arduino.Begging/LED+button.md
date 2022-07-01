## LED + BUTTON

```cpp
 int button = 2;
 int led = 13; 
 bool estadoled = 0;

void setup()
{
  pinMode (button, INPUT_PULLUP);
  pinMode(led, OUTPUT);
}

void loop()
{
  if (digitalRead(button) == LOW)
  {
    estadoled = !estadoled;
    digitalWrite (led, estadoled);
    while (digitalRead(button) == LOW);
    delay (100);
  }
}
```

