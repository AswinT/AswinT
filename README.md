# 🚀 Aswin T — Building sleek web experiences, one commit at a time


  



  



  
  
  
  


***

## 🧭 What I’m about

- Shipping fast, refactoring smarter, documenting just enough.  
- Crafting MERN apps with a TypeScript core and modern DX.  
- Exploring Next.js, GraphQL, and edge-first patterns for performance.  
- Always down for hackathons and collaborative OSS building.

> Fun fact: My coffee cools down faster than my deploys—both still get done.

***

## 🛠 Core stack


  


- Frontend: React, Next.js, Tailwind, Zustand  
- Backend: Node.js, Express, GraphQL, REST, WebSockets  
- Data: MongoDB, Prisma, Redis (learning)  
- Tooling: TypeScript everywhere, ESLint+Prettier, Vitest/Jest, Docker

***

## ✨ Highlights

- Built full-stack prototypes that go from idea ➜ design ➜ deploy in days.  
- Strong bias toward clean API contracts, predictable state, and zero-footgun DX.  
- Love turning rough UX into delightful micro-interactions.

***

## 🧪 Current playgrounds

- Next.js + App Router + RSC for edge-ready apps  
- Type-safe APIs with tRPC/GraphQL  
- Real-time features with Socket.IO and server actions  
- Incremental static regen + caching for blazing-fast UX

***

## 📦 Featured snippets

```tsx
// server/actions/createTodo.ts (Next.js RSC pattern + Zod)
'use server'
import { z } from 'zod'
import { db } from '@/lib/db'

const Input = z.object({ title: z.string().min(1), due: z.date().optional() })

export async function createTodo(input: unknown) {
  const { title, due } = Input.parse(input)
  return db.todo.create({ data: { title, due, done: false } })
}
```

```ts
// api/todos.ts (tRPC style type-safe endpoints)
import { z } from 'zod'
export const todosRouter = {
  list: async () => fetch('/api/todos').then(r => r.json()),
  add: async (title: string) =>
    fetch('/api/todos', {
      method: 'POST',
      body: JSON.stringify({ title }),
      headers: { 'Content-Type': 'application/json' }
    }).then(r => r.json()),
}
```

***

## 📊 By the numbers


  
  



  


***

## 🌐 Elsewhere


  
  


***

## 🤝 Let’s build

- Open to hackathons, OSS sprints, and pairing on interesting bugs.  
- Got a product idea? I can turn it into a clickable prototype fast.  
- Best way to reach me: email or LinkedIn.  
