---
title: Load React component lazily
date: "2020-07-11T09:48:10.438Z"
description: "Using suspense in react"
keywords: "React, react suspence"
tag: "bite-size"
---

```javascript
const AddAReview = React.lazy(() => import('./add_a_review'));
```

* Import the component file lazily by using React.lazy .
* Now you can use AddAReview with JSX syntax.
* But if you try to use it anywhere in the current component it will first reload the component and then load it again with the new component. For ... this you can use another React component Suspence that can be used for showing the loading state of the component.
* What i think is that the React fallback to reloading the component if you don't pass any fallback or something.

* Example use:

```javascript
<Suspense fallback={<div>Loading...</div>}>
    <AddAReview />
</Suspense>
```

> Just putting it in the web because i fear the publish button.
