


> [!important] Qu'est ce qu'un file d'exécution ?
> En Java, un **thread** (ou **fil d’exécution**) est la plus petite unité d’exécution traitée indépendamment par le système d’exploitation. Il représente une séquence d’instructions pouvant être exécutée en parallèle d’autres threads, permettant l’exécution concurrente de tâches dans une application.


### Les exeptions : 
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


> Les exeptions sont gérées en JAVA grâces aux blocs : 
 
 ``` 
 try {
 
 } catch {
 
 }  
 ```


> Pour générer une exception, il suffit d'utiliser le mot clé throw, suivi d'un objet dont la classe dérive de **Throwable**. Si l'on veut générer une exception dans une méthode avec throw, il faut l'indiquer dans la déclaration de la méthode, en utilisant le mot clé **throws**.

```
public class SaisieErroneeException extends Exception {
	public SaisieErroneeException() {
		super();
	}
	public SaisieErroneeException(String `s`) {
		super(s);
	}
}
```


> Pour utiliser cette exeption nouvellement crée, ont procède de la sorte :

```
public class TestSaisieErroneeException {
	public static void controle(String chaine) throws
	SaisieErroneeException {
		if (chaine.equals("") == true)
			throw new SaisieErroneeException("Saisie erronee : chaine
			vide");
		}

public static void main(java.lang.String[] args) {
	String chaine1 = "bonjour";
	String chaine2 = "";
	try {
		controle(chaine1);
	} catch (SaisieErroneeException e) {
		System.out.println("Chaine1 saisie erronee");
	}
	try {
		controle(chaine2);
	} catch (SaisieErroneeException e) {
		System.out.println("Chaine2 saisie erronee");
	}
}
```

### printStackTrace() :
---
>La méthode printStackTrace() en Java est utilisée pour afficher la pile d’appels (stack trace) d’une exception ou d’une erreur dans la console. C’est une méthode disponible dans la classe de base des exceptions, Throwable, que toutes les exceptions et erreurs héritent en Java.
>

### getMessage() :
---
> La méthode .getMessage(), permet de renvoyer le message d'erreur renvoyer lors de la capture d'une exeption.
> 