# Next.js 15 App Router Dynamic Layout Issue

This repository demonstrates a subtle bug in Next.js 15's App Router where data fetched within `getServerSideProps` doesn't dynamically update the layout if the data determines the components or structure of the layout.  The solution involves refactoring to use client-side fetching or a more appropriate data fetching mechanism that integrates with layout updates.

## Bug

The initial render shows data fetched from the API.  If you change the data dynamically that would alter the layout structure, the layout does not reflect that change.  This is because `getServerSideProps` is only executed once on the server during initial load.

## Solution

The solution involves client-side fetching of data, ensuring that changes to the layout are handled accordingly in response to updated client-side data.
