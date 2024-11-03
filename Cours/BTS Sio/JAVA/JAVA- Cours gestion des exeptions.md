


> [!important] Qu'est ce qu'un file d'exécution ?
> En Java, un **thread** (ou **fil d’exécution**) est la plus petite unité d’exécution traitée indépendamment par le système d’exploitation. Il représente une séquence d’instructions pouvant être exécutée en parallèle d’autres threads, permettant l’exécution concurrente de tâches dans une application.


### Les éxeptions : 
---
>En Java, une **exception** est un événement indésirable qui se produit durant l’exécution d’un programme et qui interrompt son flux normal. Les exceptions peuvent être causées par divers facteurs, tels que des erreurs de logique, des ressources manquantes ou des conditions imprévues.
>


```
try {

    int result = 10 / 0; // Cela déclenche une ArithmeticException

} catch (ArithmeticException e) {

    System.out.println("Erreur : Division par zéro.");

}
```


> Les exeption sont gérées en JAVA grâces aux blocs : 
 
 ``` 
 try {
 
 } catch {
 
 }  
 ```