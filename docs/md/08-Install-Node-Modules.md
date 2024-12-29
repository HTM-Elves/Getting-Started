<section
  id="install-node-modules"
  aria-labelledby="install-node-modules"
  data-item="Install Node Modules"
>
  <h2><a href="#install-node-modules">Install Node Modules</a></h2>


The `newTutorial.js` script, and the `filter.js` and `watch.js` scripts inside the `public/` folder, require a number of third-part Node Modules to run. These are listed as `"devDependencies"` in the `package.json file.

<details class="note" open>
<summary>npm scripts</summary>
The `package.json` file also contains a block called `"scripts"`. When you execute the command `npm run demo` in the Terminal, npm (the Node Package Manager) will run the associated script: `node newTutorial.js Demo`.

You will be using `npm` commands like this often in the future.

</details>

To install the `devDependencies` that HTM-Elves require: 

1. In a Terminal window open on your `MyTutorial.github.io` directory, run:
   
   ```bash-#w
   npm i
   ```
   (`i` is short for `install`. You can run `npm install` if you prefer, but `i` is quicker.)

![Installing the devDependencies](images/npm_i.webp)

After a burst of activity in the Terminal window, a new folder named `node_modules/` and a new file named `package-lock.json` should appear inside your `MyTutorials.github.i` folder.

<details
class="pivot"
open
>
<summary>Scripts and Dependencise</summary>
The `package.json` file acts as the command centre for the repository. It has two sections which will make the whole workflow work:

* `"scripts"` provides two commands that you can use to generate a tutorial Template
* `"devDependencies"` defines the node modules that will make all the magic happen.

However, there are two other services that HTM-Elves relies on, and these need to be installed at a global level. The next step explains how to do this.

</details>
</section>