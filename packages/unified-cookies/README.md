# next-unified-cookies

> Unified cookie management for both server and client in Next.js is achievable with a "single implementation."

#### Client

```jsx
"use client";

import { cookies } from "next-unified-cookies";

export const Client = () => {
  return <p>client: {cookies().get("name")}</p>;
};
```

#### Server

```jsx
import { cookies } from "next-unified-cookies";

export default function Page() {
  const cookie = cookies().get("name");

  return (
    <>
      <p>server: {cookie}</p>
      <Client />
    </>
  );
}
```

## Installation

```bash
$ npm install next-unified-cookies
```

### Spec:

> We will follow the official Next.js documentation for handling cookies as described in the "API Reference for the cookies function." By adhering to these guidelines, we ensure our implementation is robust and up-to-date with Next.js standards.

For more details, please refer to the official documentation: [Next.js cookies function API Reference](https://nextjs.org/docs/app/api-reference/functions/cookies).

#### `cookies().get(key)`

Retrieves the value of the specified cookie key.

#### `cookies().getAll()`

Retrieves all cookies.

#### `cookies().set(key, value, options)`

Sets a cookie with the specified key, value, and options.

#### `cookies().delete(key)`

Deletes the cookie with the specified key.

#### `cookies().has(key)`

Checks if a cookie with the specified key exists.