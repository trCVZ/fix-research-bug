## Bug : Mise à jour de l'index `sequence1Index`

Une ligne manquait dans le code. 
Sans la ligne ci-dessous, `sequence1Index` ne revenait pas au bon endroit et continuer d'avancer dans le tableau `sequence1`. Par exemple dans le cas ou sequence1 est 11112 et sequence2 est 1112, `sequence1Index` continuait d'avancer dans le tableau `sequence1` et ne retournait pas au deuxième index de `sequence1`.

```javascript
// Ajout de la ligne pour que sequence1Index retourne au bon index
this.sequence1Index = this.sequence1Index - this.sequence2Index + 1
```