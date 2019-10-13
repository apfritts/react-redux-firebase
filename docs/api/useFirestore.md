<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [useFirestore][1]
    -   [Examples][2]

## useFirestore


React hook that return firestore object.
Firestore instance is gathered from `store.firestore`, which is attached
to store by the store enhancer (`reduxFirestore`) during setup of
[`redux-firestore`][4]

### Examples

_Basic_

```javascript
import React from 'react'
import { useFirestore } from 'react-redux-firebase'

export default function AddData({ firebase: { add } }) {
  const firestore = useFirestore()

  function addTodo() {
    const exampleTodo = { done: false, text: 'Sample' }
    return firestore.collection('todos').add(exampleTodo)
  }

  return (
    <div>
      <button onClick={addTodo}>
        Add Sample Todo
      </button>
    </div>
  )
}
```

Returns **[object][5]** Extended Firestore instance

[1]: #usefirestore

[2]: #examples

[3]: https://react-redux-firebase.com/docs/api/useFirestore.html

[4]: https://github.com/prescottprue/redux-firestore

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object