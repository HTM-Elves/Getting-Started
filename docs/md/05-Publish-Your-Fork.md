<section
id="publish-your-fork"
aria-labelledby="publish-your-fork"
data-item="5. Publish Your Fork"
>
<h2><a href="#publish-your-fork">Publish Your Fork on GitHub</a></h2>

At the end of the previous step, your should find yourself on the home page of your newly-forked repository. Notice that there is a file called `index.html`.

![The contents of your new repository](images/index.webp)

When you use GitHub Pages to publish your newly-forked repository, it is this `index.html` file which will be used to create the home page. The repository also contains a `private/` directory which contains a script, a CSS file and a JSON file that will be used to customize the `index.html` page.

The `public/` directory contains files that can be used by future repositories that you will create for your tutorials.

To publish the repository:

1. Click on the Settings tab at the top right of the page. (You may have to click on a `...` button if the page is too narrow to show all the tabs.)
2. In the menu column on the left, click on the Pages link
3. In the Build and Deployment section, make sure that the `main` branch is selected, and choose the `/(root)` directory as the source.
4. Click on Save

![Publishing with GitHub Pages](images/GitHubPages.webp)

GitHub will queue your publish request, so you may have to wait a few minutes before the new page is ready. You should find it at `https://MyTutorials.github.io` (where you replace `MyTutorials` with the actual name of your new Organization).

The home page of your new Organization should look something like this:

![A placeholder Welcome page](images/Welcome.webp)

<details
class="pivot"
open
>
<summary>Placeholder Tutorials</summary>
The default home page is just a placeholder. It provides some dummy links to tutorials that you haven't written yet. They will highlight as you roll your mouse over them, but they will not take you anywhere. You will see later how you can customize this page.

For now, this page's existence proves two things:

* You succeeded in using GitHub Pages to publish a home page for your new organization
* The files in the `public/` folder are accessible to the Organization as a whole. The icons beside each dummy tutorial link are stored inside the `public/` folder, and the `index.html` file in at the root of your repository is able to show them.

In the next steps , you'll see how to create a Demo tutorial and publish it to your new Organization.

</details>
</section>