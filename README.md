# Press 💌

Press is an experimental literate code tool. Press processes literate code files like Literate JS or Literate Ruby into regular source.

Press uses Markdown and an added `.md` extension to source files so they're readable in GitHub & GitLab, and uses `.gitattributes` settings so your source's detected language stays the same.

Press works for any language.

## Using Press

*Press is a work in progress, so this is to come.*

Install Press with [npm](https://www.npmjs.com/get-npm):

```bash
npm install --save-dev press-literate
```

Set up & use Press:

```bash
npx press init
npx press source/hello.js.md lib/
```

`press init` sets your repo to recognize `.js.md` files as JS using your `.gitattributes` file. You only need to run it once per project. After that, you can use Press with the options below to process your literate code.

## Press options

Use Press with the `press` command in your npm scripts, or directly using `npx press`.

💁‍♂️

## Writing literate code

To read best on GitHub & GitLab, using [GitHub-flavored Markdown](https://guides.github.com/features/mastering-markdown/) is recommended. Press converts any fenced or indented Markdown code blocks to code, and (by default) comments out prose to preserve line numbers.

For proper syntax highlighting, it's recommended to use fenced code blocks with a language set, like so:

~~~markdown
# Hello

Prints a nice little greeting.

```js
console.log("hello!")
```
~~~

Then give your code an added `.md` extension, like `hello.js.md` for example, which becomes `hello.js` with its prose commented out after running it through Press.

## Pressfiles

Out of the box, Press supports JS & TypeScript. Use Pressfiles to add support for any language to Press.

For example, to add Press support for Ruby, we'd make a Pressfile `.press` at the root of our project like so:

```json
[
  {
    "language": "ruby",
    "extensions": ["rb"],
    "comment": "#"
  }
]
```

When Press comes across a `.rb.md` file, it'll convert it to a `.rb` file, convert code blocks to regular source, and prefix every line of prose with `#` and a space. Using the `language` name, it'll also set your repo to recognize `.rb.md` files as `ruby`. The name should match a name or alias in [Linguist](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

Pressfiles also support using block comments, like so:

```json
[
  {
    "language": "c",
    "extensions": ["c"],
    "blockCommentStart": "/*",
    "blockCommentEnd": "*/"
  }
]
```

After modifying your Pressfile, you'll need to run `press init` again.

## Literate code?

A lot is lost when we write code—our reasoning, our constraints, our mental process. [Literate code](https://en.wikipedia.org/wiki/Literate_programming) lets our code express both what we're trying to do, as well as how it was done and why. Let's make software both user- & developer-friendly.

Press uses Markdown for literate code as it's readable on the web, easy to pick up, and so it can stay hands-off in how you decide to define literate for you.

Maybe one day, we'll even see a `.litjs`.

A bit more on literate code & the motivation behind Press [here](LITERATE.md).

😊
