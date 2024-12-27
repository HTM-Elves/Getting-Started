<section
id="a-demo-tutorial"
aria-labelledby="a-demo-tutorial"
data-item="8. A Demo Tutorial"
>
<h2><a href="#a-demo-tutorial">A Demo Tutorial</a></h2>

As you saw earlier, the `package.json` file contains a script called `"demo"`. It's time to test it.

1. In the Terminal window that you have open on your `MyTutorials.github.io` folder, run the command:

   ```bash-#w
   npm run demo
   ```

If everything is properly installed, your browser should open showing a ready-made four-part tutorial. The content is a condensed version of this tutorial, without all the details.

![Create a demo tutorial with a single command](images/RunDemo.webp)

Just like this tutorial that you are reading now, this demo tutorial has the following features:

* A menu on the left which collapses to a hamburger if the viewport is not wide enough to show both the menu and the content.
* A toggle button at the top of the menu that allows you to choose between showing the tutorial as a single page, or split into sections.
* Two links at the foot of the menu (which don't work yet, because you haven't created the associated GitHub repository)
* A footer at the end of each section which allows you to navigate to the next section
* Coloured collapsible blocks with information that you can skip over if you are in a hurry.
* The month in which the tutorial was created in the top right corner.
* Numbered and bullet lists, headers and other formatting.
  
### A Separate Repository
The Demo tutorial has been created in a folder inside the  parent folder shared with your `MyTutorials.github.io` folder. The subfolder `docs/md/` contains a number of Markdown files with the `.md` extension.

The Demo folder also contains its own `package.json` file, which has its own `"scripts"`:

```json
{
  "scripts": {
    "pandoc": "pandoc -o docs/index.html --template=public/template.html docs/md/*.md",
    "watch": "node public/watch.js Demo"
  }
}
```

The `"pandoc"` script runs the Markdown-to-HTML conversion progress. As you'll see shortly, the `"watch"` can be used to run the `"pandoc"` script every time a Markdown file changes.

### Conversion on Command

The `npm run demo` command that you typed first created all these files, and then triggered the `"pandoc"` command in the new `package.json` file. As a result, the file at `docs/index.html` was created automatically. It is this `index.html` file which is now showing in your browser.

![The `docs/md/` folder](images/docs_md.webp)

<details
class="note"
open
>
<summary>Markdown File Numbering System</summary>
The Markdown files are numbered with zero-padded numbers, to make sure that they are treated in the correct order. However, counter-intuitively, the very first file (`99-Introduction.md`) has the _highest_ number. This is because of the way the page sections need to be handled by CSS. This issue is dealt with in more detail in the tutorial [Writing Your Own Tutorials](https://htm-elves.github.io/Writing-Your-Own-Tutorials/).

</details>

### Reading from the `public/` folder

The `index.html` file contains links to files inside the folder at `MyTutorial.github.io/public/`. Specifically, it reads in a number JavaScript files, CSS files, and some SVG icons.

<details
class="pivot"
  open
>
<summary>Summary</summary>
The `npm run demo` command also initialized a Git repository inside the Demo folder, and made a first `commit`. 

In the next step, you will push this repository to your Tutorials Organization, so that you can publish the `index.html` file with GitHub Pages.

</details>
</section>