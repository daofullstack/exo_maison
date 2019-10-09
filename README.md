# exo_maison
 
## Exercice  1 : 
Convertir une phrase en son acronyme.
Les techniciens aiment leur TLA (acronymes en trois lettres).
Aidez à générer du jargon en écrivant un programme qui convertit un nom long tel que NOT A NUMBER en son acronyme (NAN).

    String maPhrase = "Not A Number";
    List ph =maPhrase.split(" ");
    ph.forEach((f)=>print(f[0]);)
 
 ********************************************************************************
 


##Exercice 2 :
Un numéro Armstrong est un nombre qui correspond à la somme de ses propres chiffres, chacun étant élevé à la puissance du nombre de chiffres.
Par exemple:
•	9 est un nombre Armstrong, parce que 9 = 9^1 = 9
•	10 n'est pas un nombre Armstrong, car10 != 1^2 + 0^2 = 1
•	153 est un nombre Armstrong, parce que: 153 = 1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153
•	154 n'est pas un nombre Armstrong, car:154 != 1^3 + 5^3 + 4^3 = 1 + 125 + 64 = 190
    
    bool amstron(int number) {
        var stringNum = number.toString();
        return number == stringNum.split('').map((x) => pow(int.parse(x), stringNum.length)).reduce((a, b) => a + b);
    }
    var isAmstrong =amstron(10);
    print(isAmstrong);
*****************************************************************************************************

##Exercice 3 : 
Gouttes de pluie
Convertit un nombre en chaîne dont le contenu dépend des facteurs du nombre.
•	Si le nombre a 3 comme facteur, indiquez «Pling».
•	Si le nombre a 5 comme facteur, indiquez «Plang».
•	Si le nombre a 7 comme facteur, indiquez «Plong».
•	Si le nombre n’a pas un facteur de 3, 5 ou 7, il suffit de passer directement les chiffres du nombre.
Exemples
•	Les facteurs de 28 sont 1, 2, 4, 7 , 14, 28.
o	En termes de gouttes d'eau, ce serait un simple "Plong".
•	Les facteurs de 30 sont 1, 2, 3 , 5 , 6, 10, 15, 30.
o	En termes de gouttes d'eau, ce serait un "PlingPlang".
•	34 a quatre facteurs: 1, 2, 17 et 34.
•	En termes de gouttes d'eau, ce serait "34".
  •	                  var foo=34;
  •	                  (foo % 3 ==0 )? ((foo % 5 ==0 )? 
  •	                      ( (foo % 7 ==0 )? print("pling plong plang"): print("pling plong"))
  •	                        :( foo % 7==0)? print("pling plang"):print("pling"))
  •	                  :(foo % 5 ==0)? (( foo % 7==0)? print("plong plang") :print("plong")) 
  •	                  :(foo % 7 ==0)? print("plang"): print(foo);

*******************************************************************************************
##Exercice 4 : 

Nombre de mots
Étant donné une phrase, comptez les occurrences de chaque mot dans cette phrase.
Par exemple pour l'entrée "NAN NAN est une école Atypique"
NAN: 2
est: 1
une: 1
ecole: 1
Atypique : 1

          String maPhrase = "NaN NaN Not A Number";
          List ph =maPhrase.split(" ");
           Map map = Map();
            ph.forEach((element)=> map[element]= map.containsKey(element) ? (map[element] +=1):(1));
            print("voici les ocurrences $map");


