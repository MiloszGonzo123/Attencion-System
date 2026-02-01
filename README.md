# Mini Attencion-System

Stworzyłem System Atencji, stworzony w roblox studio.


## Jak Działa Ten System:

System składa sie z dwóch komponentów: 1. API 2. NeuralNetwork

##### *API:*
 ma kilka zadań, a dokładniej to normalizacje danych:

 słowo: "pies" lub zdanie "pies kalkulator kosz"

 1. tokenizacja
 wszystkie zdania są  tokenizowane na osobne tokeny
 2. Positional
 każdy z tokenów ma przypisaną mu kolejność w zdaniu



##### *Neural:*
 serce Attencion,

 składa sie z 12 wejść(Input Layer)
 składa sie z 2 warst ukrytych(Hidden Layers)
 składa sie z 1 warsty wyjściowej(Output Layer)

 sieć ma jedno zadanie: obliczyć atencje dla danego tokena, od 1 do 0

 np: słowo "pies" będzie miało atencje 0.852 a słowo "fontanna" będzie miało 0.487

 Warstwa Ukryta składa sie z dwóch warstw, pierwsza warstwa składa sie z 20 neuronów
 a druga składa sie z 15 neuronów

## Trenowanie

Sieć była Trenowana przez ~+500 przykładów atencji oraz wbudowany
w nią algorytm .Train(TD)

Dodatkowo: Sieć ma o wiele mniej neuronów by uniknąć OverTraining, aby sieć nie nauczyła sie na pamięć całej tabeli trainingData

## Uwagi:

Sieć nie ma na celu liczyć atencji w zdaniu tylko ma liczyć jak bardzo słowo jest ważne, prawdopodobonie tej sieci nie da sie użyć w modelach językowych 
 
