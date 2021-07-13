This repo is used to reproduce a bug when using Tailwind CLI with JIT

[Issue Link](https://github.com/tailwindlabs/tailwindcss/issues/4969) 

----

### What version of Tailwind CSS are you using?

2.2.4

### What build tool (or framework if it abstracts the build tool) are you using?

N/A

### What version of Node.js are you using?

v12.16.1

### What browser are you using?

N/A

### What operating system are you using?

macOs

### Reproduction repository

https://github.com/juanpasolano/tailwind-layer-bug

### Describe your issue

I am using the tailwind CLI to compile files that then feeds into post CSS, like it is suggested here: https://tailwindcss.com/docs/just-in-time-mode#it-just-doesn-t-seem-to-work-properly

However, we are running into an issue where tailwinds output compiled filed contains/exports with tthe `@layer` as shown in the image.
![Screen Shot 2021-07-13 at 1 59 24 PM](https://user-images.githubusercontent.com/1621720/125509751-f53cdf25-848f-4913-9dc6-a561102b4fb2.png)
So when this file gets into postCSS it breaks.

IMPORTANT: The problem seems to be only happening when using the JIT mode. And also it only happens when we trigger a change from the HTML or any purged file.
