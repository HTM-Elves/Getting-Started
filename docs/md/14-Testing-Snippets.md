<!-- Testing Snippets -->
<section
  id="testing-snippets"
  aria-labelledby="testing-snippets"
  data-item="Testing Snippets"
>
  <h2><a href="#testing-snippets">Testing Snippets</a></h2>
  
Here's how you can test the power of snippets.

1. In the `Demo/docs/md/` folder, create a new file named `12.3-Let's_Test_Snippets!.md`
2. In the file, type `sss` and then press the Tab key. You should see the following HTML block inserted in the file:

```md-#
<!-- Let's Test Snippets! -->
<section
  id="Let's Test Snippets!"
  aria-labelledby="Let's Test Snippets!"
  data-item="Let's Test Snippets!"
>
  <h2><a href="#Let's Test Snippets!">Let's Test Snippets!</a></h2>
  

</section>
```

The _prefix_ `sss` triggered the wonderful snippet (shown below) that you just added to your `markdown.json` file. I chose `sss` as the prefix trigger, because `section` starts with an `"s"`, and I'm too lazy to move more than one finger.

```json-w
<i>"dynamic section":{
	"body": [
		"<!-- ${1:${TM_FILENAME/(^[0-9 ._-]+)|(\\..{1,4}$)|([a-z0-9]+)|([ _-]+)|(.)/${3}${4:+ }${5}/gi}} -->\n<section\n  id=\"${2:${1/([a-z0-9]+)|([\\s_.-]+)|(.)/${1:/downcase}${2:+-}/gi}}\"\n  aria-labelledby=\"$2\"\n  data-item=\"${3:${1/([\\s_\\.-]+)|('\\w(?=(?:\\s|$)))|(\\w+)/${1:+ }$2${3:/capitalize}/g}}\"\n>\n  <h2><a href=\"#$2\">${4:${3/([_\\.-]+)|('\\w(?=(?:\\s|$)))|(\\w+)/${1:+ }$2${3:/capitalize}/g}}</a></h2>\n  $0\n\n</section>"
	],
	</i><b>"prefix": "sss"</b><i>,
	"description": "id+data-item+header from file name"
}</i>
```

You don't need to worry now about _how_ this monstrosity works. However, you can already see that:

* It read in the name of the Markdown file
* It stripped the numbers from the beginning and the `.md` extension from the end
* It converted all the underscore `_` characters to spaces.

But not everything is perfect yet. As an `id`, the string `"Let's Test Snippets!"` is not ideal. So now for some magic.

1. Press the Tab key again.

Immediately, the `id`, `aria-labelledby`, and `href` values get sanitized.

```md-w
<i><!-- Let's Test Snippets! -->
<section
  id="</i><b><u>lets-test-snippets</u></b><i>"
  aria-labelledby="</i><b><u>lets-test-snippets</u></b><i>"
  data-item="Let's Test Snippets!"
>
  <h2><a href="#</i><b><u>lets-test-snippets</u></b><i>">Let's Test Snippets!</a></h2>
  

</section></i>
```

* They are converted to lowercase
* The spaces are replaced by dashes: `-`
* Non-alphanumeric characters like the apostrophe `'` and the exclamation mark `!` are removed.
* The `href` is given a leading hash character: `#`
* All three entries are selected, allowing you to edit them all at once if you want to.

4. Press the Tab key again.

```md-w
<i><!-- Let's Test Snippets! -->
<section
  id="lets-test-snippets"
  aria-labelledby="lets-test-snippets"
  data-item="</i><b><u>Let's Test Snippets!</u></b><i>"
>
  <h2><a href="#lets-test-snippets"></i><b><u>Let's Test Snippets!</u></b><i></a></h2>
  

</section></i>
```

This time the entries for `data-item` and the `<h2>` link text are selected. You can change them both at the same time, if you wish. The value for `data-item` is used in the menu, so it should be quite short.

5. Press the Tab key a fourth time.
```md-w
<i><!-- Let's Test Snippets! -->
<section
  id="lets-test-snippets"
  aria-labelledby="lets-test-snippets"
  data-item="Let's Test Snippets!"
>
  <h2><a href="#lets-test-snippets"></i><b><u>Let's Test Snippets!</u></b><i></a></h2>
  

</section></i>
```

Now only the  the `<h2>` link text is selected, so you can create a longer header for the section, if that is appropriate.

6. Press the Tab key one last time. The cursor moves to just beneath the `<h2>` tag. If you type something here, it gets added to your page.

```md-#
<!-- Let's Test Snippets! -->
<section
  id="lets-test-snippets"
  aria-labelledby="lets-test-snippets"
  data-item="Let's Test Snippets!"
>
  <h2><a href="#lets-test-snippets">Let's Test Snippets!</a></h2>
  Now let's start writing some tutorials!

</section>
```

![Your new page, already with its own menu item](images/UsingSnippets.webp)

<details class="pivot" open>
<summary>Time saving with HTM-Elves</summary>
Thanks to Markdown snippets, it's taken you only a few simple gestures to create a new page and integrate it into the output `index.html` page, along with its own entry in the menu. 

Check out the official [VS Code Snippet documentation](https://code.visualstudio.com/docs/editor/userdefinedsnippets) for more details on how to write your own snippets..

To publish the latest version of your Demo tutorial, all you need to do is commit your changes and push them to GitHub.

After this short introduction, I hope that you can already see how HTM-Elves can motivate you to share you knew knowledge with your colleagues and the world in general. 

</details>
</section>