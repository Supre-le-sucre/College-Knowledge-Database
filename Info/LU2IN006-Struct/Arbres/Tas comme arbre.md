## Définition
On définit un tas comme suit: #!
Un tas est un [[Arbres binaires]] ordonné: tous les nœuds, autre que la racine, on tune "priorité" plus grande que leur père 
<!--ID: 1715184202453-->


**Remarque**: La racine d'un tas est donc forcément l'élément minimum de celui-ci, quant au feuille, l'une d'entre elle représente le plus grand élément.

### Choix de conception
Sans perte de généralité, nous allons considérer en général, des tas représenté comme des arbres "tassé à gauche"

#### Définition
On dit d'un arbre binaire qu'il est tassé à gauche lorsque: #!
Tous ses niveaux sont <u>complets</u> mis à part le niveau inférieur, qui est complet à gauche.
<!--ID: 1715184202454-->


#### Propriété
La taille d'un arbre tassé à gauche constitué de $n$ nœuds est de #!
$$\lfloor \log_2(n)\rfloor$$
## Représentation par tableau
Pour un tas, représenté comme un arbre binaire tassé à gauche, on observe le tableau `tab` suivant: #!

Le tableau `tab` décrit chaque étage du tas en le lisant étage par étage:
- `tab[0]` indique la taille du tas (nombre de nœuds)
- `tab[1]` représente la racine du tas
- `tab[2*i]` renvoie le fils gauche du $i^{ème}$ nœud
- `tab[2*i+1]` renvoie le fils droit du $i^{ème}$ nœud
- `tab[i/2]` renvoie le père du $i^{ème}$ nœud
**Remarque**: Un tableau est donc suffisant pour représenter l'intégralité de la structure
<!--ID: 1715184202456-->


De manière général, un tas représenté comme un arbre $n$-aire tassé à gauche, on observe le tableau `tab` suivant: #!
- `tab[0]` indique la taille du tas (nombre de nœuds)
- `tab[1]` représente la racine du tas
- `tab[n*i]` renvoie le fils gauche du $i^{ème}$ nœud
- `tab[n*i+(n-1)]` renvoie le fils droit du $i^{ème}$ nœud
- `tab[i/n]` renvoie le père du $i^{ème}$ nœud
<!--ID: 1715184202458-->


## Maintien de la cohérence
Pour maintenir la cohérence du tas on utilise l'algorithme suivant: #!

Lors de l'insertion d'un élément, si celui-ci a une priorité plus faible que le pair, alors on `swap` le père avec le fils, et on continue jusqu'à ce que la cohérence soit maintenue
<!--ID: 1715184202459-->



## Annexes C

On considère un tas tassé à gauche représenté en un tableau

### Définissons de la structure
```c
#define MAX_CAPACITY 10

typedef struct {
	int tab[MAX_CAPACITY+1];	
} Tas;
```

#### Initialisation
```c
Tas* init() {
	Tas* t = malloc(sizeof(Tas));
	t.tab[0] = 0
}
```

### Algorithmes atomiques
Ces fonctions renvoies les indices du tableau correspondants
```c
int hasPere(int i) { return i!=1; }
int filsGauche(int i) { return 2*i; }
int filsDroit(int i) { return 2*i+1; }
int pere(int i) { return i/2; }
```

On a donc les fonctions booléennes suivante:
```c
int taille(Tas* t) {
	return t->tab[0];
}

int isNoeud(Tas* t, int i) {
	return i <= taille(t);
}

int hasFilsGauche(Tas* t, int i) {
	return isNoeud(t, filsGauche(i));
}

int hasFilsDroit(Tas* t, int i) {
	return isNoeud(t, filsDroit(i));
}

int estFeuille(Tas* t, int i) {
	return !hasFilsGauche(t, i);
}
```

### Maintien de cohérence
#### Echange de noeuds
Pour maintenir la cohérence on se dote de la fonctions de permutation de nœud:
```c
void echanger(Tas* t, int i, int j) {
	int tmp = tab[i];
	tab[i] = tab[j];
	tab[j] = tmp;
}
```

#### Monter un nœud d'indice i
On veut monter l'élément d'indice i si nécessaire.
```c
void monter(Tas* t, int i) {
	if(!hasPere(t, i)) return;

	int papa = pere(i);
	if(t->tab[papa] > t->tab[i]) {
		// Maintient de la cohérence
		echanger(t, i, papa);
		monter(t, papa); // On continue si nécéssaire
	}
}
```
La complexité de cet algorithme est en $\Theta(\log_2(n))$

### Trouver le plus petit fils de i
Pour trouver le plus petit fils de $i$, il suffit de parcourir un seul étage.
La fonction suivante renvoie l'indice du plus petit fils de $i$
```c
int plusPetitFils(Tas* t, int i) {
	if(! hasFilsDroit(t,i)) {
		return filsGauche(i);
	} else {
		int fg = filsGauche(i);
		int fd = filsDroit(i);
		return (tab->tab[fg] < t->tab[fd]) ? fg : fd;
	}
}
```

### Descendre un nœud d'indice i
On veut descendre l'élément d'indice i si nécéssaire
```c
void descendre(Tas* t, int i) {
	if(isFeuille(t, i)) return;

	int fiston = plusPetitFils(t, i);
	if(t->tab[i] > t->tab[fiston]) {
		// Maintient de la cohérence
		echanger(t, i, fiston);
		descendre(t, fiston); // On continue si nécéssaire
	}
}
```
La complexité de cet algorithme est en $\Theta(\log_2(n))$

### Utilitaires

#### Minimum
```c
int min(Tas* t) {
	return t->tab[1];
}
```

#### Insertion
```c
void insert(Tas* t, int priorite) {
	t->tab[0]++;
	t->tab[t->tab[0]] = priorite
	monter(t, t->tab[0]);
}
```
La complexité de cet algorithme est en $\Theta(\log_2(n))$
#### Suppression du minimum
```c
void suppMin(Tas* t) {
	echanger(t, t->tab[0], 1);
	t->tab[0]--;
	descendre(t, 1)
}
```
La complexité de cet algorithme est en $\Theta(\log_2(n))$