<section
id="fork-htm-elves"
aria-labelledby="fork-htm-elves"
data-item="4. Fork HTM-Elves"
>
<h2><a href="#fork-htm-elves">Fork HTM-Elves to your New Organization</a></h2>

The [HTM-Elves.github.io repository](https://github.com/orgs/HTM-Elves/repositories) contains all the tools that you will need both on GitHub and on your local development computer.

On GitHub, it will provide the CSS, JavaScript and icon files that will be public by all your online tutorials. On your development computer, it will provide scripts to automate your tutorial creation process.

First, you'll need to create a _fork_ of [HTM-Elves.github.io repository](https://HTM-Elves.github.io) in your new GitHub Organization.

<details
class="note"
open
>
<summary>Forks and Clones</summary>
When you clone a GitHub repository, you create an identical copy of the files on your local computer. When you _fork_ a GitHub repository, you create an identical copy of the files _in a different account on GitHub_. If you are the owner of the account, then you have full control of your newly forked repository.

To work with your forked repository, you will still need to clone it to your development computer, just as you are used to doing.

</details>

To create your own fork of `HTM-Elves.github.io`:

1. Visit [the HTM-Elves.github.io repository page](https://github.com/HTM-Elves/HTM-Elves.github.io)
2. Find the Fork button, click on the contextual menu button, and select Create A New Fork

![Create a new fork](images/CreateFork.webp)

1. A new page will open.
   * From the Owner contextual menu, choose the name of the Organization that you have just created.
   * In the Repository Name field, enter the exact name of the Organization that you have just created, followed by `.github.io`.
   For example, if you created an Organization called "MyTutorials", then the repository name **must** be "MyTutorials.github.io" (case is not important). This tells GitHub to use this repository to create [the home page for your Organization](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites). If the following steps fail to work for you, check that you have named your repository correctly.

![Select the owner organization and set the name of the fork repository](images/NewFork.webp)

<details
class="pivot"
open
>
<summary>A Fork with Two Roles</summary>
You can now use [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) to generate an online page for your tutorials Organization from your forked repository. You can also clone the repository to your development computer, and use it to generate tutorial repositories for your Organization.

These roles will be treated in the next sections.

</details>
</section>