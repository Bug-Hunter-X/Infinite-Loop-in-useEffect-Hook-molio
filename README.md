# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by an incorrect `useEffect` dependency array.

The `bug.js` file contains the buggy code.  The `useEffect` hook attempts to update the `count` state within itself, creating an infinite loop. This is because the empty dependency array `[]` means the effect runs only once after the initial render, and it immediately triggers a re-render, starting the cycle anew. 

The `bugSolution.js` file provides the corrected code.