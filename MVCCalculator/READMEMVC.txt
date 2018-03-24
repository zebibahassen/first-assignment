Name: Zebiba Hassen
Id: ATR/6348/08
Section: 2

SIMPLE ADDER JAVA APP

CalculatorModel.java

The Model performs all the calculations needed
and that is it. It doesn't know the View
exists

CalculatorView.java

This is the View
Its only job is to display what the user sees
It performs no calculations, but instead passes
information entered by the user to whomever needs
it.

CalculatorController.java

The Controller coordinates interactions
between the View and Model