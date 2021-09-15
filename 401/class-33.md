# NextJs
## Create a Next.js App:
To build a complete web application with React from scratch, there are many important details you need to consider:
Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
You need to do production optimizations such as code splitting.
You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
You might have to write some server-side code to connect your React app to your data store.
A framework can solve these problems. But such a framework must have the right level of abstraction — otherwise it won’t be very useful. It also needs to have great "Developer Experience".

## Next.js: The React Framework:
Next.js has the best-in-class "Developer Experience" and many built-in features; a sample of them are:
An intuitive page-based routing system (with support for dynamic routes)
Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
Automatic code splitting for faster page loads
Client-side routing with optimized prefetching
Built-in CSS and Sass support, and support for any CSS-in-JS library
Development environment with Fast Refresh support
API routes to build API endpoints with Serverless Functions
Fully extendable
Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.
## Assets, Metadata, and CSS:

Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.
The public directory is also useful for robots.txt, Google Site Verification, and any other static assets.
Download Your Profile Picture
First, let's retrieve your profile picture.
Download your profile picture in .jpg format (or use this file).
Create an images directory inside of the public directory. Save the picture as profile.jpg in the public/images directory.
The image size can be around 400px by 400px.
You may remove the unused SVG logo file directly under the public directory.

## Unoptimized Image
With regular HTML, you would add your profile picture as follows:
<img src="/images/profile.jpg" alt="Your Name" />
However, this means you have to manually handle:
Ensuring your image is responsive on different screen sizes
Optimizing your images with a third-party tool or library
Only loading images when they enter the viewport
And more. Instead, Next.js provides an Image component out of the box to handle this for you.

## Image Component and Image Optimization:
Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.
Automatic Image Optimization works with any image source. Even if the image is hosted by an external data source, like a CMS, it can still be optimized.
Using the Image Component
Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.
Images are lazy loaded by default. That means your page speed isn't penalized for images outside the viewport. Images load as they are scrolled into viewport.
Images are always rendered in such a way as to avoid Cumulative Layout Shift, a Core Web Vital that Google is going to use in search ranking.
Here's an example using next/image to display our profile picture. The height and width props should be the desired rendering size, with an aspect ratio identical to the source image.

## Metadata

What if we wanted to modify the metadata of the page, such as the < title> HTML tag?
< title > is part of the < head> HTML tag, so let's dive into how we can modify the < head> tag in a Next.js page.
Open pages/index.js in your editor and find the following lines:

<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>

Notice that < Head > is used instead of the lowercase < head>. < Head> is a React Component that is built into Next.js. It allows you to modify the < head> of a page.
You can import the Head component from the next/head module.
Adding Head to first-post.js We haven't added a <title> to our /posts/first-post route. Let's add one.
Open the pages/posts/first-post.js file and add an import for Head from next/head at the beginning of the file:
import Head from 'next/head'
Then, update the exported FirstPost component to include the Head component. For now, we‘ll add just the title tag:
export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}

Try accessing http://localhost:3000/posts/first-post. The browser tab should now say “First Post”. By using your browser’s developer tools, you should see that the title tag is added to < head>.

## CSS Styling
As you can see, our index page (http://localhost:3000) already has some styles. If you take a look at pages/index.js, you should see code like this:

<style jsx>{`
  …
`}</style>

This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).
Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.

