<section
id="clone-your-fork"
aria-labelledby="clone-your-fork"
data-item="6. Clone Your Fork"
>
<h2><a href="#clone-your-fork">Clone Your Fork to your Development Computer</a></h2>

For now, everything you have done has been on the GitHub site. Now it's time to make a clone of your `MyTutorial.github.io` repository on your local computer. This will allow you to generate a demo tutorial and publish it.

To clone your forked repository to your development computer:

1. On the home page of your new repository, click on the green Code button and copy the link to the repository.

![Copy the URL of the remote repository](images/CloneFork.webp)

1. On the desktop of your computer, create a new folder which you will use to hold all the repositories for your tutorials Organization. I'll simply call mine `MyTutorials`, like the name of my Organization.
2. Open this new folder with VS Code, and open a new Terminal, type `git clone ` and then paste the link you have just copied.
3. Press the Enter key

![Clone the repository to your development computer](images/LocalClone.webp)

### What's in the Repository
To explore the contents of your repository you can
1. Type `code -r M` then press the Tab key. (If your repository is not called `MyTutorials`, just type the first letter of your repository name instead of the `M`). Pressing the Tab key will make the Terminal autocomplete the name of the folder that has just been created.
2. Press Enter
3. In VS Code's Explorer open up all the subfolders, so you can see their contents. I'll explain these in due course.
4. Click on `package.json`

![The contents of the repository](images/packege-json.webp)

<details
class="pivot"
open
>
<summary>Scripts and Dependencise</summary>
The `package.json` file acts as the command centre for the repository. It has two sections which will make the whole workflow work:

* `"scripts"` provides two commands that you can use to generate a tutorial Template
* `"devDependencies"` defines the node modules that will make all the magic happen.

In the next step, you will be installing these dependencies, as well as the services that they rely on.

</details>

</section>