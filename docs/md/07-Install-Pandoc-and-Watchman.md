<section
id="install-pandoc-and-watchman"
aria-labelledby="install-pandoc-and-watchman"
data-item="7. Pandoc and Watchman"
>
<h2><a href="#install-pandoc-and-watchman">Install Pandoc and Watchman</a></h2>

The HTM-Elves workflow relies on Pandoc, a free open-source software document converter. It can convert between any of about 60 document formats, including Markdown and HTML (which is the focus here), but also PDF, DOCX, PowerPoint, EPUB and many others that you may one day encounter.

Pandoc is designed to be run from the Command Line, but HTM-Elves takes care of all the details for you, 

<details
class="warn"
open
>
<summary>Install Pandoc</summary>

You must install Pandoc on your development computer before continuing. Without Pandoc, there will be no magic.

**Follow the [installation instructions here](https://pandoc.org/installing.html).**

</details>

To work most efficiently, it is good to see your Markdown files converted to HTML files and displayed in your browser in real time. For this, you can install [Meta's open source Watchman service](https://facebook.github.io/watchman/).

<details
class="warn"
open
>
<summary>Install Watchman?</summary>
It's possible that Watchman has already been installed on your system by another development tool that you use. To check, run this command in a Terminal window:

```bash
watchman --version
```

If you see a response like `command not found: watchman`, then you will need to [install Watchman](https://facebook.github.io/watchman/docs/install) yourself. If you see a version number, like `2024.11.04.00`, you're already set. 

</details>

When you have installed these two services, you can install the Node modules that the HTM-Elves project will use to control them.

<details
class="warn"
open
>
<summary>Installing Node Modules</summary>
**In a Terminal window open on your `MyTutorials.github.io` folder, run the command:**
```bash-#w
npm i
```
This will tell `npm` to install all the `devDependencies` listed in `package.json`.

</details>

<details
class="pivot"
open
>
<summary>Ready to Generate a Demo Tutorial</summary>
If you have succeeded in installing Pandoc, Watchman and the required Node modules correctly, the fun is about to begin.  

</details>
</section>  