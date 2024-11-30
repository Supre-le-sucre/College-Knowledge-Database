La linéarisation de LAD-LASSO est la même que celle de [[LAD|LAD]] sauf qu'on essaye ici de minimiser le nombre de paramètre non-nul. On cherche donc à pénaliser l'existence de ces paramètre

On pose alors cette fois un paramètre $\lambda > 0$ qui est d'autant plus grand qu'on cherche à réduire le nombre de paramètre non nuls

$$
\text{minimiser } \quad \sum_{i=1}^{n}\left| y_{i} - \beta_{0} - \sum_{j=1}^{p}\beta_{j}x_{ij}  \right| + \lambda \sum_{i=1}^{p} 
$$