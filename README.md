# Press 💌

Press is an experimental literate code tool. Press processes literate code files like Literate JS or Literate Ruby into regular source.

Press uses Markdown and an added `.md` extension to source files so they're readable in GitHub & GitLab, and uses `.gitattributes` settings so your project's language breakdown stays the same. At the moment, Press is built for JS projects.

## Using Press

*Press is a work in progress, so this is to come.*

Install Press:

```bash
yarn add --dev press-literate

# or with npm
npm install --save-dev press-literate
```

Set up & use Press:

```bash
npx press initla
npx press source/hello.md.js lib
```

`press init` sets your repo to recognize `.js.md` files as JS using your `.gitattributes` file. You only need to run it once per project. After, you can use `press` with the options below to process your literate code.

## Press options

💁‍♂️

## Writing literate code

Press converts any fenced or indented Markdown code blocks to code, and (by default) comments out prose to preserve line numbers. For proper syntax highlighting, it's recommended to use fenced code blocks with a language set, like so:

~~~markdown
# Hello

Prints a nice little greeting.

```js
console.log("hello!")
```
~~~

Then give your code an added `.md` extension, like `hello.md.js` for example, which becomes `hello.js` with its prose commented out after running it through Press.

## Literate code?

A lot is lost when we write code—our reasoning, our constraints, our mental process. Literate code lets our code express both what we're trying to do, as well as how it was done and why. Opinionated? Maybe. I'm big on software being both user- & developer-friendly.

Press uses Markdown for literate code as it's readable on the web, easy to pick up, and so it can stay hands-off in how you decide to define literate for you.

😊
