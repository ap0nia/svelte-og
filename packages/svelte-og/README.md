# @ap0nia/vercel-og

> Modified version of @vercel/og that's compatible with SvelteKit

## Getting Started

1. Install the library.
```bash
npm install @ap0nia/svelte-og
```

2. Return a dynamically generated OpenGraph image response from a server endpoint.
```ts
// src/routes/og/+server.ts

import { SvelteImageResponse } from '@ap0nia/svelte-og'
import type { RequestHandler } from './$types'
import Og from '$lib/components/og.svelte'

export const GET: RequestHandler = async () => {
  return new SvelteImageResponse(Og)
}
```
