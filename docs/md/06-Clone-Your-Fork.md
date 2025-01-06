<section
id="clone-your-fork"
aria-labelledby="clone-your-fork"
data-item="Clone Your Fork"
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

The contents of your parent `MyTutorials` directory should now look like this:

```bash-#w
MyTutorials
└── MyTutorials.github.io
    ├── LICENSE
    ├── README.md
    ├── index.html
    ├── newTutorial.js
    ├── package.json
    ├── private
    │   ├── script.js
    │   ├── styles.css
    │   └── tutorials.json
    └── public
        ├── filter.js
        ├── media-queries.css
        ├── nodoc.svg
        ├── prism
        ├── script.js
        ├── storage.js
        ├── styles.css
        ├── svg
        ├── template.html
        └── watch.js
```

<details class="pivot" open>
<summary>Completing the set-up</summary>
There are three more steps before HTM-Elves will be ready to work on your development computer:

* Obtaining a GitHub personal access token, so that you can delegate GitHub house-keeping duties to HTM-Elves
* Installing the Node Modules that the HTM-Elves scripts require
* Installing two services —Pandoc itself and Meta's Watchman— to which HTM-Elves outsource all the hard work.

Next step: the personal access token.

</details>

</section>