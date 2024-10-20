## Théorème de la méthode de Newton
On a le théorème suivant: #!

Soit $\phi: I \to \mathbb R$  une fonction de classe $\mathcal C^2$ et $x^* \in I$ tel que $\phi(x^*) = 0$ et $\phi'(x^*) \not = 0$. Alors il existe $\epsilon > 0$ tel que $\forall x_0 \in ]x^* - \epsilon, x^* + \epsilon[$ la suite $$x_{n+1} = x_n - \frac{\phi(x_n)}{\phi'(x_n)}$$Converge vers $x^*$ avec pour $0<M< \frac{1}{\epsilon}$ $$|x_n -x^*| \leq \frac{1}{M}(M, |x_n - x_0|)^{2^n}$$La convergence de cette suite est donc quadratique.
<!--ID: 1729460118383-->
