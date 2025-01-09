# DateTimePicker

`DateTimePicker` est un composant React simple permettant de choisir la date qu'on souhaite via un petit calendrier qui s'affiche en dessous de l'input. Il permet également de formater la date au format par defaut : `YYYY-MM-DD` par ce format : `MM/DD/YYYY`.

Je pourrai peut être faire une mise à jour pour pouvoir choisir le format que l'on souhaite plus tard.

---

## Installation

Installez la bibliothèque via npm ou yarn :

```bash
npm install date-picker
# ou
yarn add date-picker
```

---

## Utilisation

Voici un exemple d'utilisation de `DatePicker` :

```javascript
import React, { useState } from "react";
import DatePicker from "date-picker";

function App() {
  const [date, setDate] = useState("");

  const handleDateChange = (formattedDate) => {
    console.log("Date sélectionnée :", formattedDate);
    setDate(formattedDate);
  };

  return (
    <div>
      <h1>Sélectionnez une date</h1>
      <DatePicker value={date} onChange={handleDateChange} />
      <p>Date sélectionnée : {date}</p>
    </div>
  );
}

export default App;
```

---

## API du Composant

### Props

| Prop       | Type       | Description                                                                                 | Obligatoire |
| ---------- | ---------- | ------------------------------------------------------------------------------------------- | ----------- |
| `value`    | `string`   | La date initiale au format `MM/DD/YYYY`.                                                    | Non         |
| `onChange` | `function` | Fonction de rappel appelée lorsque la date change, recevant la date au format `MM/DD/YYYY`. | Non         |

---

## Fonctionnalités

1. **Sélection de la date voulu via un calendrier**

   - Affiche un calendrier sous l'input souhaité
   - Peut choisir le mois ainsi que l'année facilement

2. **Gestion automatique des formats** :

   - Affiche la date au format `YYYY-MM-DD` dans le champ de saisie HTML.
   - Retourne la date au format `MM/DD/YYYY` via la prop `onChange`.

3. **Synchronisation automatique** :

   - Met à jour l'état interne (`date`) lorsque la prop `value` change.

---

## Méthodes Utilitaires

### `formatToDisplay(dateStr)`

- **Entrée** : Une chaîne de caractères au format `YYYY-MM-DD`.
- **Sortie** : Une chaîne de caractères au format `MM/DD/YYYY`.

### `formatToInput(dateStr)`

- **Entrée** : Une chaîne de caractères au format `MM/DD/YYYY`.
- **Sortie** : Une chaîne de caractères au format `YYYY-MM-DD`.

---
