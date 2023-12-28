# 📝 NextJS Notes 📝

## 1 - Getting Started

### What is Next.js

Next.js is a **React framework** for building full-stack web applications. You use React Components to build user interfaces, and **Next.js for additional features and optimizations**.

Under the hood, Next.js also **abstracts** and **automatically configures** tooling needed for React, like **bundling**, **compiling**, and more. This allows you to focus on building your application instead of spending time with configuration.

### Main Features

Some of the main Next.js features include:

| Feature | Description |
| --- | --- |
| Routing | A file-system based router built on top of Server Components that supports layouts, nested routing, loading states, error handling, and more. |
| Rendering | Client-side and Server-side Rendering with Client and Server Components. Further optimized with Static and Dynamic Rendering on the server with Next.js. Streaming on Edge and Node.js runtimes. |
| Data Fetching | Simplified data fetching with async/await in Server Components, and an extended fetch API for request memoization, data caching and revalidation. |
| Styling | Support for your preferred styling methods, including CSS Modules, Tailwind CSS, and CSS-in-JS |
| Optimizations | Image, Fonts, and Script Optimizations to improve your application's Core Web Vitals and User Experience. |
| TypeScript | Improved support for TypeScript, with better type checking and more efficient compilation, as well as custom TypeScript Plugin and type checker. |

### App Router vs Pages Router

Next.js has **two different routers**: the **App Router** and the **Pages Router**. 

The App Router is a newer router that **allows you to use React's latest features**, such as Server Components and Streaming. 

The Pages Router is the original Next.js router, which **allowed you to build server-rendered React applications** and continues to be supported for older Next.js applications.

## 2 - Installation

### System Requirements

- [Node.js 18.17](https://nodejs.org/) or later.
- macOS, Windows (including WSL), and Linux are supported.

### Automatic Installation

```bash
npx create-next-app@latest
```

On installation, you'll see the following prompts:

```bash
What is your project named? my-app
Would you like to use TypeScript? No / Yes
Would you like to use ESLint? No / Yes
Would you like to use Tailwind CSS? No / Yes
Would you like to use `src/` directory? No / Yes
Would you like to use App Router? (recommended) No / Yes
Would you like to customize the default import alias (@/*)? No / Yes
What import alias would you like configured? @/*
```

After the prompts, `create-next-app` will create a folder with your project name and install the required dependencies.

### Manual Installation

To manually create a new **Next.js app**, install the required packages:

```bash
npm install next@latest react@latest react-dom@latest
```

Open your `package.json` file and add the following `scripts`:

```bash
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }
}
```

These scripts refer to the different stages of developing an application:

- `dev`: runs `[next dev](https://nextjs.org/docs/app/api-reference/next-cli#development)` to start Next.js in development mode.
- `build`: runs `[next build](https://nextjs.org/docs/app/api-reference/next-cli#build)` to build the application for production usage.
- `start`: runs `[next start](https://nextjs.org/docs/app/api-reference/next-cli#production)` to start a Next.js production server.
- `lint`: runs `[next lint](https://nextjs.org/docs/app/api-reference/next-cli#lint)` to set up Next.js' built-in ESLint configuration.

**Creating Directories**

Next.js uses file-system routing, which means the routes in your application are determined by how you structure your files.

**The `app` Directory**

For new applications, we recommend using the **App Router**. 

This router allows you to use React's latest features and is an evolution of the **Pages Router** based on community feedback.

Create an `app/` folder, then add a `layout.tsx` and `page.tsx` file. These will be rendered when the user visits the root of your application (`/`).

Create a **root layout** inside `app/layout.tsx` with the required `<html>` and `<body>` tags:

```tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  )
}
```

Finally, create a home page `app/page.tsx` with some initial content:

```tsx
export default function Page() {
  return <h1>Hello, Next.js!</h1>
}
```

> **Good to know**: If you forget to create `layout.tsx`, Next.js will automatically create this file when running the development server with `next dev`.
> 

**The `pages` Directory (Optional)**

If you prefer to use the Pages Router instead of the App Router, you can create a `pages/` directory at the root of your project.

Then, add an `index.tsx` file inside your `pages` folder. This will be your home page (`/`):

```tsx
export default function Page() {
  return <h1>Hello, Next.js!</h1>
}
```

Next, add an `_app.tsx` file inside `pages/` to define the global layout. Learn more about the [custom App file](https://nextjs.org/docs/pages/building-your-application/routing/custom-app).

```tsx
import type { AppProps } from 'next/app'
 
export default function App({ Component, pageProps }: AppProps) {
  return <Component {...pageProps} />
}
```

Finally, add a `_document.tsx` file inside `pages/` to control the initial response from the server. Learn more about the [custom Document file](https://nextjs.org/docs/pages/building-your-application/routing/custom-document).

```tsx
import { Html, Head, Main, NextScript } from 'next/document'
 
export default function Document() {
  return (
    <Html>
      <Head />
      <body>
        <Main />
        <NextScript />
      </body>
    </Html>
  )
}
```

Learn more about [using the Pages Router](https://nextjs.org/docs/pages/building-your-application/routing/pages-and-layouts).

**The `public` folder (Optional)**

Create a `public` folder to store static assets such as images, fonts, etc. Files inside `public` directory can then be referenced by your code starting from the base URL (`/`).

### Run the Development Server

1. Run `npm run dev` to start the development server.
2. Visit `http://localhost:3000` to view your application.
3. Edit `app/page.tsx` (or `pages/index.tsx`) file and save it to see the updated result in your browser.

## 3 - Building Your Application

### Routing

**Routing Fundamentals**

The skeleton of every application is routing. This page will introduce you to the **fundamental concepts** of routing for the web and how to handle routing in Next.js.

**Terminology**

First, you will see these terms being used throughout the documentation. Here's a quick reference:

[terminology-component-tree.avif](NextJS%20bbcf058765a249c0bc242641f610757e/terminology-component-tree.avif)

- **Tree:** A convention for visualizing a hierarchical structure. For example, a component tree with **parent** and **children** components, a **folder structure**, etc.
- **Subtree:** Part of a tree, **starting at a new root** (first) and **ending at the leaves** (last).
- **Root**: The **first node** in a **tree** or **subtree**, such as a root layout.
- **Leaf:** **Nodes** in a **subtree** that have **no children**, such as the last segment in a URL path.

[terminology-url-anatomy.avif](NextJS%20bbcf058765a249c0bc242641f610757e/terminology-url-anatomy.avif)

- **URL Segment:** Part of the URL path delimited by slashes.
- **URL Path:** Part of the URL that comes after the domain (composed of segments).

**The `app` Router**

In version 13, Next.js introduced a new **App Router** built on [React Server Components](https://nextjs.org/docs/app/building-your-application/rendering/server-components), which supports **shared layouts**, **nested routing**, **loading states**, **error handling**, and more.

The App Router works in a new directory named `app`. The `app` directory works alongside the `pages` directory to allow for incremental adoption. This allows you to opt some routes of your application into the new behavior while keeping other routes in the `pages` directory for previous behavior. If your application uses the `pages` directory, please also see the [Pages Router](https://nextjs.org/docs/pages/building-your-application/routing) documentation.

> **Good to know**: The App Router takes priority over the Pages Router. Routes across directories should not resolve to the same URL path and will cause a build-time error to prevent a conflict.
> 

[next-router-directories.avif](NextJS%20bbcf058765a249c0bc242641f610757e/next-router-directories.avif)

By default, components inside `app` are [React Server Components](https://nextjs.org/docs/app/building-your-application/rendering/server-components). This is a performance optimization and allows you to easily adopt them, and you can also use [Client Components](https://nextjs.org/docs/app/building-your-application/rendering/client-components).

> **Recommendation:** Check out the [Server](https://nextjs.org/docs/app/building-your-application/rendering/server-components) page if you're new to Server Components.
> 

**Roles of Folders and Files**

Next.js uses a file-system based router where:

- **Folders** are used to define routes. A route is a single path of nested folders, following the file-system hierarchy from the **root folder** down to a final **leaf folder** that includes a `page.js` file. See [Defining Routes](https://nextjs.org/docs/app/building-your-application/routing/defining-routes).
- **Files** are used to create UI that is shown for a route segment. See [special files](https://nextjs.org/docs/app/building-your-application/routing#file-conventions).

**Route Segments**

Each folder in a route represents a **route segment**. Each route segment is mapped to a corresponding **segment** in a **URL path**.

[route-segments-to-path-segments.avif](NextJS%20bbcf058765a249c0bc242641f610757e/route-segments-to-path-segments.avif)

**Nested Routes**

To create a nested route, you can nest folders inside each other. For example, you can add a new `/dashboard/settings` route by nesting two new folders in the `app` directory.

The `/dashboard/settings` route is composed of three segments:

- `/` (Root segment)
- `dashboard` (Segment)
- `settings` (Leaf segment)

**File Conventions**

Next.js provides a set of special files to create UI with specific behavior in nested routes:

| layout | Shared UI for a segment and its children |
| --- | --- |
| page | Unique UI of a route and make routes publicly accessible |
| loading | Loading UI for a segment and its children |
| not-found | Not found UI for a segment and its children |
| error | Error UI for a segment and its children |
| global-error | Global Error UI |
| route | Server-side API endpoint |
| template | Specialized re-rendered Layout UI |
| default | Fallback UI for Parallel Routes |

> **Good to know**: `.js`, `.jsx`, or `.tsx` file extensions can be used for special files.
>

---

## Server Side Rendering

> Also referred to as **SSR** or **Dynamic Rendering**.

If a page uses **Server-side Rendering**, the page HTML is generated on **each request**.

To use **Server-side Rendering** for a page, you need to `export` an `async` function called `getServerSideProps`. This function will be called by the server on every request.

For example, suppose that your page needs to **pre-render frequently updated data** (fetched from an external API). You can write `getServerSideProps` which fetches this data and passes it to `Page` like below:

```jsx
export default function Page({ data }) {
  // Render data...
}
 
// This gets called on every request
export async function getServerSideProps() {
  // Fetch data from external API
  const res = await fetch(`https://.../data`)
  const data = await res.json()
 
  // Pass data to the page via props
  return { props: { data } }
	}
```

As you can see, `getServerSideProps` is similar to `getStaticProps`, but the difference is that `getServerSideProps` is run on every request instead of on build time.

## Client Side Rendering

> Also referred as **CSR** or **Static Rendering.**

In **Client-Side Rendering (CSR)** with React, the browser downloads a **minimal HTML page** and the **JavaScript needed** for the page. The JavaScript is then used to update the DOM and render the page. 

When the application is **first loaded**, the user may notice a slight delay before they can see the full page, this is because the page isn't fully rendered until all the JavaScript is downloaded, parsed, and executed.

After the page has been loaded for the first time, navigating to other pages on the same website is typically **faster**, as only necessary data needs to be fetched, and JavaScript can re-render parts of the page **without** requiring a **full page refresh**.

In Next.js, there are two ways you can implement client-side rendering:

1. Using React's `useEffect()` hook inside your pages instead of the server-side rendering methods (`getStaticProps` and `getServerSideProps`).
2. Using a data fetching library like [SWR](https://swr.vercel.app/) or [TanStack Query](https://tanstack.com/query/latest/) to fetch data on the client (recommended).

Here's an example of using `useEffect()` inside a Next.js page:

```jsx
import React, { useState, useEffect } from 'react'
 
export function Page() {
  const [data, setData] = useState(null)
 
  useEffect(() => {
    const fetchData = async () => {
      const response = await fetch('https://api.example.com/data')
      if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`)
      }
      const result = await response.json()
      setData(result)
    }
 
    fetchData().catch((e) => {
      // handle the error as needed
      console.error('An error occurred while fetching the data: ', e)
    })
  }, [])
 
  return <p>{data ? `Your data: ${data}` : 'Loading...'}</p>
}
```

In the example above, the component starts by rendering `Loading...`. Then, once the data is fetched, it re-renders and displays the data.

Although fetching data in a `useEffect` is a pattern you may see in older React Applications, we recommend using a data-fetching library for better performance, caching, optimistic updates, and more. Here's a minimum example using [SWR](https://swr.vercel.app/) to fetch data on the client:

```jsx
import useSWR from 'swr'
 
export function Page() {
  const { data, error, isLoading } = useSWR(
    'https://api.example.com/data',
    fetcher
  )
 
  if (error) return <p>Failed to load.</p>
  if (isLoading) return <p>Loading...</p>
 
  return <p>Your Data: {data}</p>
}
```

> **Good to know**:
> 
> Keep in mind that CSR can impact SEO. Some search engine crawlers might **not** execute JavaScript and therefore only see the initial empty or loading state of your application. It can also lead to performance issues for users with slower internet connections or devices, as they need to wait for all the JavaScript to load and run before they can see the full page. Next.js promotes a hybrid approach that allows you to use a combination of server-side rendering, static site generation, and client-side rendering, **depending on the needs of each page** in your application. In the App Router, you can also use Loading UI with Suspense to show a loading indicator while the page is being rendered.