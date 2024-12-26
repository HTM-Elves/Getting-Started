<section
id="publish-your-fork"
aria-labelledby="publish-your-fork"
data-item="Publish Your Fork"
>
<h2><a href="#publish-your-fork">Publish Your Fork on GitHub</a></h2>

At the end of the previous step, your should find yourself on the home page of your newly-forked repository. Notice that there is a directory called `docs`.

![The docs directory](images/docs.webp)

Inside the `docs/` directory is a file called `index.html`.

![The index.html file](images/docs_index.webp)

When you use GitHub Pages to publish your newly-forked repository, it is this `index.html` file which will be used to create the home page. In the same `docs/` directory, there is an `assets/` directory which contains a script and a CSS file that will be used to customize the `index.html` page.

To publish the repository:

1. Click on the Settings tab at the top right of the page. (You may have to click on a `...` button if the page is too narrow to show all the tabs.)
2. In the menu column on the left, click on the Pages link
3. In the Build and Deployment section, make sure that the `main` branch is selected, and choose the `/docs` directory as the source.
4. Click on Save

![Publish with GitHub Pages](images/GitHubPages.webp)

GitHub will queue your publish request, so you may have to wait a few minutes before the new page is ready. You should find it at `https://MyTutorials.github.io` (where you replace `MyTutorials` with the actual name of your new Organization).



<details
class="pivot"
open
>
<summary>Summary</summary>


</details>
</section>