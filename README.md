# AntD + Next.js + tRPC + SSR = 😞

This is a [T3 Stack](https://create.t3.gg/) project bootstrapped with `create-t3-app`. It is a minimal reproduction of this bug.

## Usage

```
npm i
npm run dev
```

Output when visiting app:

```
TypeError: useInsertionEffect only works in Client Components.
Add the "use client" directive at the top of the file to use it.
Read more: https://nextjs.org/docs/messages/react-client-hook-in-server-component
```

This can be resolved by removing `ssr: true` in `src/utils/api.ts` (line 51), but we want SSR to work.
