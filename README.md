# React Native FlatList - Incorrect Key Prop

This repository demonstrates a common but subtle bug in React Native's FlatList component: using the index as the key prop for list items. This leads to inefficient rendering and potential data inconsistencies. The solution showcases how to use unique identifiers as keys for correct list behavior.

## Bug Description
Using `index` as the `key` prop in FlatList is a widespread error. When data updates occur (addition, deletion, or modification of items), using the index doesn't allow React Native to efficiently update the list because indices change on each update. This leads to incorrect item rendering or missing updates. 

## Solution
To fix this, you must use a unique identifier for each item in your data array. This could be a database ID, UUID, or any other property that guarantees uniqueness.