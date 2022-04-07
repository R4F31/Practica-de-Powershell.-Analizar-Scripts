# Practica-de-Powershell.-Analizar-Scripts

## Ejercicio 1

 Codigo y comentario del script
 
#Se crea una variable de tipo entero que tiene el valor de 1

$number = 1
 
#Se mostrara por pantalla el string "El numero es:" y a continuancion se concadena  con la variable anterior
Write-Host "The number is: " $number

#Se crea una variable de tipo entero que tiene el valor de 2

$number = 2

 
#Se mostrara por pantalla el string "El numero es:" y a continuancion se concadena  con la variable anterior
Write-Host "The number is: " $number

#Se crea una variable de tipo entero que tiene el valor de 3

$number = 3
 
#Se mostrara por pantalla el string "El numero es:" y a continuancion se concadena  con la variable anterior
Write-Host "The number is: " $number

#Se crea una variable de tipo entero que tiene el valor de 4

$number = 4
 
#Se mostrara por pantalla el string "El numero es:" y a continuancion se concadena  con la variable anterior
Write-Host "The number is: " $number


## Ejercicio 2

#Se crea una variable que sera del tipo integer llamada repeat y tendra el valor de 5

[int]$repeat = 5

#Con un bucle for, se escribira por pantalla "hello" 6 veces,  ya que se repetira hasta condicion sea igual a 5,
la variable $counter se ira  incrementando  en 1

for ($counter = 0; $counter -lt $repeat; $counter++) {
    Write-Host "hello"
} 


#Con un bucle while, mientras contador sea menor a $repeat, se escribira por pantalla "hello", y  se incrementará en 1 
la variable $counter

[int]$repeat = 5
[int]$counter = 0

while ($counter -lt $repeat) {
    Write-Host "hello"
    $counter++
}


#Con un bucle do while, se ejecuta al menos una vez y luego  se ira ejecutando  mientras contador sea menor a repeat, en cada vuelta del  bucle while el contador se ira incrementando  en 1

[int]$repeat = 5
[int]$counter = 0
do {
    Write-Host "hello"
    $counter++
}
while ($counter -lt $repeat) 


#Se declara una variable de tipo string

[string]$stringOfCharacters = "PowerShell for Beginners"

#Se ejecuta un bucle ForEach, por cada vuelta que hace el bucle la variable character se convierte en la ultima letra del string y esto se imprime por pantalla. Vendria siendo un for recorriendo un array item por item.

foreach ($character in $stringOfCharacters.ToCharArray()) {
    Write-Host $character
} 

#Se declara una variable de tipo string y se ejecuta un bucle ForEach-Object y por cada vuelta que da  el bucle imprime  por pantalla el carácter en el que se encuentra.

[string]$stringOfCharacters = "PowerShell for Beginners"

$stringOfCharacters.ToCharArray() | ForEach-Object { Write-Host "$_" }


#Ejercicio 3


#Si 4 es igual a 4 se ejecutará lo que esta entre corchetes

if (4 -eq 4) {
    Write-Host "4 is equal to 4"
}



#Si el string "hello" es igual al string "hello" se ejecutará lo que esta entre corchetes

if ("hello" -eq "hello") {
    Write-Host "Both strings are equal to each other"
} 



#Se declaran dos variables una llamada "x" y la otra "y" de tipo integer las dos con valor 10

[int]$x = 10
[int]$y = 10



#Si las variables "x" y "y" son iguales se ejecutará lo que esta entre corchetes

if ($x -eq $y) {
    Write-Host "the x and y variables are equal to each other"
}


#Si las dos variables no son iguales se ejecutara  lo que esta entre corchetes

else {
    Write-Host "The x and y variables are NOT equal to each other"
}



#Se declara una variable, que tendra por string el valor "Ian"

$yourName = "Ian"




#Si el valor de la variable es igual a "Ian" se ejecutara lo que esta entre corchetes

if ($yourName -eq "Ian") {
    Write-Host "Hay my name is Ian too!"
}

#En caso de que el nombre no sea "Ian" se ejecutara lo que esta entre corchetes.

else {
    Write-Host "Hi $yourName, nice to meet you!"
}


#Se crea la variable playerInput, que sera de tipo string y esta vacia

[string]$playerInput = ""




#Se imprime por pantalla un mensaje y se espera que el usuario introduzca un valor

$playerInput = Read-Host -Prompt "You walk into a room with two doorways. One to the left and one to the right. Type 'left' or 'Right' to walk through one of the doors."

#Si lo que ha introducido  es igual a "left" se ejecutará lo que esta entre corchetes
if ($playerInput -eq "left") {
    Write-Host "Player typed left"
}


#Si lo que ha introducido es igual a "right" se ejecutará lo que esta entre corchetes
elseif ($playerInput -eq "right") {
    Write-Host "Player typed right"
}

En caso de que lo introducido no cumpla ninguna de las dos condiciones anteriores se ejecutara lo que ensta entre corchetes

else {
    Write-Host "Player typed something we didn't understand"
}



## Operadores de comparación

#-eq	es  Equals y lo que hace es compararar dos valores en este caso compara si el valor 5 es igual a 5	

if (5 -eq 5) {
}
   
   
   
#-ne es  not equals,y lo que hace es comparar que dos valores no sean iguales en este caso  compara si el valor 3 no es igual a 4

if (3 -ne 4) {
}
   
   
   
#-gt Greater than,lo que hace es comparar si el primer parametro es mas grande que el segundo en este caso  compara si el valor 4 es mas grande que 2

if (4 -gt 2) {
}
   
#-ge Greater than or equal, lo que hace es comparar si el primer valor es mayor o igual al segundo valor, en este caso  compara si el valor 2 es mayor o igual a 1

if (2 -ge 1) {
}
   
   
#-lt Less than,lo que hace es comparar si el primer valor es mas pequeño que el segundo en este caso compara si el valor 1 es mas pequeño que 2

if (1 -lt 2) {
}

#-le Less than or equal,lo que hace es comparar si el primer valor es mas pequeño o igual al segundo valor en este caso  compara si el valor 1 es mas pequeño o igual a 2

if (1 -le 2) {
} 

#-like nos compara si el primer string  empieza por el string a comparar, el asterisco nos permite solo introducir la parte que queremos comparar y no el resto de esta manera decimos que queremos buscar que diga hello y no nos importa si es helloww

if ("hello how are you?" -like "hello*") {
}

#-notlike, compara si el string inicial no es igual al otro string

if ("HELLO" -notlike "BYE") {
} 


#-match, nos compara si dentro del string hay alguna letra o palabra igual a la que queremos 

if ("HELLO" -match "H") {
    Write-Host "H exists in the string HELLO"
}
   
#-notmatch, nos compara si dentro del string  no hay alguna letra o palabra igual a la que queremos 

if ("HELLO" -notmatch "A") {
    Write-Host "A does not match in the string HELLO"
}


#-contains	nos devuelve true si dentro de la lista esta el valor que hemos indicado

$list = @(1, 2, 3, 4, 5)

if ($list -contains 3) {
    #the list does contain a 3
}

#-notcontains, nos retorna true si dentro de la lista no esta el valor que hemos indicado

$list = @(1, 2, 3, 4, 5)

if ($list -notcontains 8) {
    #$list does not contain 8
}


#-in, nos retorna true si dentro de la lista contiene el valor que hemos  indicado

$list = @(1, 2, 3, 4, 5)
if (3 -in $list) {
    #the list does contain a 3
} 

#-notin, nos retorna true si dentro de la lista no contiene el valor indicado

$list = @(1, 2, 3, 4, 5)
if (6 -notin $list) {
    #6 is not in the list
}

#-is, nos retorna true si el valor indicado concide con el tipo de valor	ya sea integer, string....

$var = "This is a string"
if ($var -is [string]) {
    #The variable is a string
}

#-isnot, nos retorna true si el valor no conincide con el tipo de valor que hemos indicado	

$var = "This is a string"
if ($var -isnot [bool]) {
    #The variable is a string and not a Boolean value so results in true.
} 
   


## Declaraciones Switch


#Se declara una variable  integer con el valor 2

[int]$number = 2

#Como la variable anterior tiene valor 2 se ejecutará la condicion 2

switch ($number) {
    1 { "The number is one" }
    2 { "The number is two" }
    default { "I dont know what the number is" }
}


#Se declara una variable string con el valor "Blue" 

[string]$favouriteColour = "Blue"

#Se ejecutara la condicion que coincida con el valor de la variable anterior

switch ($favouriteColour) {
    "Red" {
        "Your favourite colour is Red"
        "I like red too."
    }
    "Blue" {
        "Your favourite colour is Blue"
        "I like Blue too."
    }
    default { "I dont recognise that colour" }
}
