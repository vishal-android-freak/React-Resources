# All About Redux

Well, it all started few months back when I was first introduced to React Native and since then Redux has been a pain. Reading for the first time, things seemed to be like a cakewalk but coming back to it after a couple of days, I could understand Greek and Latin better. So, this time I thought of writing everything down in a systematic manner which can be useful for all the lost souls, like me.

## Overview

Redux can be classified into 3 important components (not the React component)

```mermaid
graph TD;
Redux --> Store
Redux --> Actions
Redux --> Reducers
```

The game of Redux is played so that we have a single `state ` object which defines the entire state of the application. We don't define per component states and change them using `setState({})`.  

```javascript
class ReduxLove extends Component {
	constructor(props) {
		//This is no longer needed with Redux
		this.state = { 
			someInitialState: []
	    }
	}
}
```

## Redux process in a nutshell
Every component or event showing a wish to change the `state`, has to ***dispatch*** an `action` which is accepted by a `reducer` function which has been given the powers of modifying the state of the application. Every reducer function should be a **pure function**.

## What are Pure Functions?

Consider the following code snippets:
```javascript
// Pure function
function getMeSomeSortedData(garbageArray) {
	return garbageArray.map((value) => sortThisShit(value))
}
```
```javascript
function dumpInMoreGarbage(garbageBin) {
	garbageBin++;
	garbageBin 
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY2MTY5MzczNV19
-->