# React Native Asynchronous Data Fetching Bug

This repository demonstrates a common bug in React Native applications related to asynchronous data fetching and state updates.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

The issue arises because the `setState` function in React is asynchronous.  In the buggy code, the component attempts to render before the asynchronous `fetch` operation completes, resulting in displaying the initial state (null in this case) instead of the actual fetched data.

The solution involves using an appropriate loading state and ensuring the UI updates only after the data has been successfully retrieved.