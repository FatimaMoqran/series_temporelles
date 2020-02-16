# series_temporelles

   La dépendance temporelle induit une dépendance entre les variables au cours du temps, et la nécessité de fixer un cadre théorique un peu différent

-      Plusieurs façons de travailler sur une série temporelle

o  Régression brute si estimation grossière

o  Moyennes mobiles

o  La rendre « stationnaire »

-      Pour rendre une série stationnaire, deux méthodes

o  Enlever la tendance et la saisonnalité automatiquement à l’aide de packages 

o  Différencier la série à l’ordre 1 ou 2 (recommandé dans notre cas)

-      Pour tester la stationnarité d’une série, on effectue un test de Dickey-Fuller et on souhaite que la valeur du test soit la plus basse possible

-      Une fois l’ordre de différenciation déterminé (correspondant au I dans ARIMA), on cherche à déterminer les ordres p et q (AR(p) + MA(q) -> ARMA(p,q)) ;

-      Pour cela, on trace les graphiques d'autocorrélation et d'autocorrélation partielle et on regarde le comportement des valeurs lorsque l'écart grandit (cf tableau récapitulatif)

-      Lorsque p et q sont choisis, on estime le modèle ARMA à l’aide de statsmodels et on trace les résidus de l'estimation. On vérifie qu’ils sont bien stationnaires (Dickey-Fuller cf étape précédente)

-      On peut alors ré-entraîner en séparant train/test et on évalue la qualité de la prédiction

-      Si décevant, on revient à l’étape du choix de p et q et on recommence. Si toujours pas solutionné, on essaie de changer l’ordre de différenciation.

 

Ressources :

-       Tester la stationnarité d’une série :https://machinelearningmastery.com/time-series-data-stationary-python/

-      Le modèle ARIMA en Python à l’aide de statsmodels : https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/

-      Méthode de Box-Jenkins pour trouver p et q : https://en.wikipedia.org/wiki/Box–Jenkins_method

-       Rappels globaux ARMA (à lire en diagonale)https://www.math.u-psud.fr/~goude/Materials/ProjetMLF/time_series.html

 