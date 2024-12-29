<!-- Deploy with gh pages -->
<section
id="deploy-with-gh-pages"
aria-labelledby="deploy-with-gh-pages"
data-item="Deploy With GH-Pages"
>
<h2><a href="#deploy-with-gh-pages">Deploy Your First Tutorial with GitHub-Pages</a></h2>

In step [5: Publish Your Fork](#publish-your-fork), you used GitHub Pages to publish the root directory of your `MyTutorials.github.io` repository. As a result, the `index.html` file at the root of the `MyTutorials.github.io` repository became visible when you visited `https://mytutorial.github.io`. The contents of the `public/` folder also became accessible to the world in general.

In your Demo directory, the `index.html` file is generated inside the `Demo/docs/` folder. GitHub Pages allows you to publish from the `/docs` folder, which means that the other folders in the `Demo` repository will not be visible in a browser.

If you look at the file at `Demo/docs/index.html`, you will see that it references files at `../public/`. This is a relative path to `"https://MyTutorials.github.io/public/"`.

```html
<i><!DOCTYPE html>
<html lang="en">
<head></i>
```
```html-s
<!-- Some lines skipped -->
```
```html-#9
<i><title>Demo Tutorial</title>
<link rel="stylesheet" href="</i><b>../public</b><i>/styles.css">
<link rel="stylesheet" href="</i><b>../public/</b><i>media-queries.css">
<link rel="stylesheet" href="</i><b>../public/</b><i>prism/prism.css">

<script defer src="</i><b>../public/</b><i>prism/prism.js"></script>
<script defer src="</i><b>../public/</b><i>storage.js"></script>
<script defer src="</i><b>../public/</b><i>script.js"></script>
</head></i>
```
```html-s
<!-- Remaining lines skipped -->
```

This means that all your tutorials will share the same look and feel. If you change the styles in your `MyTutorials.github.io/public` folder, and push the changes to GitHub, all your tutorials will adopt the new styles.

## Deploying the `/docs` folder

In step [5: Publish Your Fork](#publish-your-fork), you had to visit the Pages section on the GitHub website, and deal with everything manually. If you created a GitHub personal access token in step [7. Personal Access Token](#github-token), then HTM-Elves can deploy the `/docs` folder of your Demo repository for you automatically.

1. Open a Terminal window in your Demo folder
2. Run the command `npm run publish`.

![Publishing your tutorial with `npm run publish`](images/RunPublish.webp)

As before, GitHub will queue your publish request, so you may have to wait a few minutes before the new page is ready. You should find it at `https://MyTutorials.github.io/Demo` (where you replace `MyTutorials` with the actual name of your tutorials Organization). The correct link should be shown in your Terminal. Ctrl-click on it to visit the page.

If you see a `404 Not Found` message, just wait a few minutes for GitHub to take care of your request, then refresh the page.

It should look something like this:

![Published!](images/Published.webp)

<details
class="pivot"
open
>
<summary>Conclusion</summary>
## _Congratulations!_

You have seen how to:

* Create your own GitHub Organization where you can publish tutorials
* Fork the HTM-Elves repository, to use as the root of your tutorial organization
* Publish your forked repository, with its dummy home page
* Clone your forked repository to your local computer
* Generate and use a GitHub personal access token
* Install Pandoc and Watchman and a set of Node modules
* Use HTM-Elves to generate a Demo tutorial automatically and push it to a new GitHub repository inside your new organization
* Use GitHub Pages to publish this new tutorial repository for the world to see.

The next step is to write a tutorial of your own, and to publish it using the same workflow. The article [Writing Your Own Tutorials](https://htm-elves.github.io/Writing-Your-Own-Tutorials/#section-snippets) is designed to show you all the tricks and shortcuts that the HTM-Elves workflow offers you, so that you can focus on your writing and building your online reputation.

## _Have fun!_

</details>
</section>