# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-   l'état (_state_) pour contrôler l'affichage d'un composant ✔️ ->  
    `const [pieceOfState, setPieceOfState] = useState(intialState)`
-   les composants enfants et les _props_ qu'on leur passe ✔️ ->  
    `<Component prop={pieceOfState}>`
-   le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️ ->

```javascript
onClick(doSomething)
onChange(doSomeOtherThing)
etc...
```

-   le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️ ->  
    When component mounts & unMounts

```javascript
useEffect(() => {
	doSomething

	return () => {
		cleanUp
	}
}, [dependencies])
```

-   l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌ / ✔️
-   l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌ / ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

Le code qui suit est un composant du projet cité ci-après

```typescript
import { FC } from 'react'
import { RefactoredRowType } from '../types'
import Message from './Message'

interface IProps {
	filteredData: RefactoredRowType[]
}

const DataRow: FC<IProps> = ({ filteredData }): JSX.Element => {
	const formatDate = (date: Date) => {
		return new Intl.DateTimeFormat('fr-FR').format(date)
	}
	const formatTime = (date: Date) => {
		return `${date.getHours()} h ${date.getMinutes()} s ${date.getMilliseconds()} ms`
	}
	return (
		<tbody>
			{filteredData.map((row, index) => {
				return (
					<tr key={`row-${index}`}>
						<td className='text-center'>
							{formatDate(row.date)}
							<br />
							{formatTime(row.date)}
						</td>
						<Message message={row.message} />
						<td className='text-center'>{row.clientIdNumber}</td>
					</tr>
				)
			})}
		</tbody>
	)
}

export default DataRow
```

### Utilisation dans un projet ❌ / ✔️

[le repo](https://github.com/Holmes-EH/datadog-csv-viewer/tree/main/src/components)

Description :
J'ai créé cette micro web app pour faire du csv parsing dédié à faire du troubleshooting de requêtes dans l'entreprise où je fais mon alternance

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

-   lien
-   description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

-   action 1 ❌ / ✔️
-   action 2 ❌ / ✔️
-   ...

Résolution :

## 📽️ J'en fais la démonstration

-   J'ai ecrit un [tutoriel](...) ❌ / ✔️
-   J'ai fait une [présentation](...) ❌ / ✔️
