# DateTimePicker

`DateTimePicker` est un composant React simple permettant de gérer et de formater des dates. Il permet de saisir une date au format `YYYY-MM-DD` tout en exposant une valeur formatée pour l'affichage au format `MM/DD/YYYY`.

---

## Installation

Installez la bibliothèque via npm ou yarn :

```bash
npm install votre-package
# ou
yarn add votre-package

Utilisation

Voici un exemple d'utilisation de DateTimePicker :

import React, { useState } from "react";
import DateTimePicker from "votre-package";

function App() {
  const [date, setDate] = useState("");

  const handleDateChange = (formattedDate) => {
    console.log("Date sélectionnée :", formattedDate);
    setDate(formattedDate);
  };

  return (
    <div>
      <h1>Sélectionnez une date</h1>
      <DateTimePicker value={date} onChange={handleDateChange} />
      <p>Date sélectionnée : {date}</p>
    </div>
  );
}

export default App;

API du Composant
Props
Prop	Type	Description	Obligatoire
value	string	La date initiale au format MM/DD/YYYY.	Non
onChange	function	Fonction de rappel appelée lorsque la date change, recevant la date au format MM/DD/YYYY.	Non
Fonctionnalités

    Gestion automatique des formats :
        Affiche la date au format YYYY-MM-DD dans le champ de saisie HTML.
        Retourne la date au format MM/DD/YYYY via la prop onChange.

    Synchronisation automatique :
        Met à jour l'état interne (date) lorsque la prop value change.

Méthodes Utilitaires
formatToDisplay(dateStr)

    Entrée : Une chaîne de caractères au format YYYY-MM-DD.
    Sortie : Une chaîne de caractères au format MM/DD/YYYY.

formatToInput(dateStr)

    Entrée : Une chaîne de caractères au format MM/DD/YYYY.
    Sortie : Une chaîne de caractères au format YYYY-MM-DD.
```
