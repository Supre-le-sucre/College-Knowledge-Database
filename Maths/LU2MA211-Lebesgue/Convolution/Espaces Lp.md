## Définition des espaces $\mathcal L^p$
On introduit les ensembles suivants: #!
$$\mathcal L^1(\mathbb R):= \{f: \mathbb R \mapsto \mathbb C : f \text{ intégrable}\}$$
$$\mathcal L^2(\mathbb R):= \{f: \mathbb R \mapsto \mathbb C : |f|^2 \text{ intégrable}\}$$
$$\mathcal C^0_b(\mathbb R):= \{f: \mathbb R \mapsto \mathbb C : f \text{ continue bornée}\}$$
<!--ID: 1714516791393-->


## Propriété principales des espaces $\mathcal L^p$
Les espaces $\mathcal L^1(\mathbb R)$ $\mathcal L^2(\mathbb R)$ et $\mathcal C^0_b(\mathbb R)$ sont des espaces vectoriels

## La norme
On définit la norme intégrale de la façon suivante: #!

$$||f||_1 := \int_\mathbb R|f|$$
$$||f||_2 := \int_\mathbb R|f|^2$$
$$||f||_\infty := \sup_\mathbb R|f|$$
## Espaces de Lebesgue
On définit les espaces de Lebesgue de la façon suivante: #!
<!--ID: 1714516791395-->


Soit $\sim$ la relation d'équivalence entre fonction de $\mathbb R \to \mathbb C$, tel que $f \sim g$ si $f=g$ presque partout.
On note $$L^1(\mathbb R) = \mathcal L^1(\mathbb R)/\sim$$$$L^2(\mathbb R) = \mathcal L^2(\mathbb R)/\sim$$

## Inégalité de Cauchy-Schwarz
On énonce l'inégalité de la façon suivante: #!

Pour $f,g \in L^2(\mathbb R)$ on a $fg \in L^1(\mathbb R)$ et: $$\left|\int_\mathbb Rf\overline g\right| \leq ||f||_2||g||_2$$ et l'égalité si et seulement si $f$ et $g$ sont liées.
<!--ID: 1714516791398-->
