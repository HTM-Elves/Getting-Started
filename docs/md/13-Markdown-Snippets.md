<!-- Markdown Snippets -->
<section
  id="markdown-snippets"
  aria-labelledby="markdown-snippets"
  data-item="Markdown Snippets"
>
<h2><a href="#markdown-snippets">Markdown Snippets</a></h2>

If you look at `MyTutorials/Demo/docs/md/99-Intro.md`, you'll see section near the top that looks like this:

```md-#8
<section
  id="introduction"
  aria-labelledby="introduction"
  data-item="Introduction"
>
  <h2><a href="#introduction">Introduction</a></h2>
```
```md-s
<!-- Some lines skipped -->
```
```md-#53
</section>
```

***"Wait a minute!"*** I hear you say. ***"This looks like HTML, but I thought that the whole point of this HTM-Elves workflow was to avoid writing any HTML!"***

You are right. You won't be _writing_ any HTML, but you will be _using_ HTML, when standard Markdown needs a little help. And Markdown needs help in creating container elements, like sections. And HTM-Elves is structured to use a `<section>` element for each logical section.

I don't want to type out chunks of HTML code each time I want a new section, or a `<details>` element or another kind of container. Instead I use [VS Code Snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) to create such chunks for me. Snippets are templates that allow you to insert predictable chunks of text, and customize them quickly depending on the context.

If you haven't used VS Code Snippets before, then you're in for a pleasant surprise. By default, though, VS Code does not provide any snippets for Markdown, and the use of snippets in Markdown files is disactivated. 

To get Markdown snippets to work for you, you need two things:

1. To activate `quicksuggestions` for Markdown files
2. A file named `markdown.json` with some useful snippets.

## Activate `quicksuggestions` for Markdown files

To activate `quicksuggestions` for Markdown files, you need to:

1. Open the VS Code's Command Palette. The lazy way is to use the menu item `View > Command Palette`, but that means that you have to move your hands away from your keyboard, which wastes time. Instead, use the keyboard shortcut `Ctrl-Shift-P`, or simply `F1`.
2. Start typing some part of "Preferences: Configure Language Specific Settings". (I find that "Lang Set" is enough to bring the appropriate command to the top of the list.)

![Configure Language Specific Settings](images/LanguageSettings.webp)

3. Press Enter. You will see a list of all the languages that VS Code can handle. Start typing "Markdown", then press Enter when Markdown appears at the top of the list.

![Markdown Settings](images/MarkdownSettings.webp)

4. In the Search bar, `@lang:markdown` will already appear. Start adding the word `quicksuggestions`, until the entry "Editor: **Quick Suggestions**" appears.

![Editor: Quick Suggestions](images/quickSuggestions.webp)

5. For the item `other`, click on the Pencil icon, which appears when you hover your mouse in the right place, then use the contextual menu to select `on`.
6. Click OK.

![Activating Markdown snippets in VS Code](images/ActivateQuickSuggestions.webp)


## Install some useful snippets

Now you can install some useful snippets in a special file called `markdown.json`. To open this file:

1. Open the VS Code's Command Palette (`Ctrl-Shift-P`, or simply `F1`).
2. Start typing "snippets", until the command "Snippets: Configure Snippets" is at the top of the list.

![Using the Command Palette to configure snippets](images/ConfigureSnippets.webp)

3. Press Enter.
4. You'll see a list of all the languages that VS Code can provide snippets for. Start typing "Markdown" until `markdown.json` is at the top of the list.

![Finding the markdown.json snippets file](images/MarkdownSnippets.webp)

5. Press Enter.
6. A file named `markdown.json` will open. It's not exactly a JSON file, because it supports JavaScript-like comments. It's probably just got comments in it and no snippets.
7. Copy the JSON from the code listing below and use this to replace the current contents of the file.
   
<details class="tip" open>
<summary>Download `markdown.json`</summary>
You can [download a complete file](markdown.json){download=""} with the Markdown snippets that help me the most, and use its contents to replace the placeholder text in your `markdown.json` file.

</details>

<details class="warn" open>
<summary>Don't overwrite existing snippets</summary>
If there are already some Markdown snippets in the file, simply add the snippets from the code listing below, rather than replacing everything.

</details>

<details class="pivot" open>
<summary>All set!</summary>
Now that you have Markdown snippets installed and activated, HTM-Elves is ready to do plenty of heavy lifting for you. But just before you start writing your own tutorials, in the next section, I'll show you just what Markdown snippets can do.

</details>

</section>
