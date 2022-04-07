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
