<!-- GitHub Token -->
<section
  id="github-token"
  aria-labelledby="github-token"
  data-item="Personal Access Token"
>
  <h2><a href="#github-token">GitHub Personal Access Token</a></h2>
  
GitHub provides an API (application programming interface) which allows you to manage your GitHub organization directly from your development computer, without visiting the GitHub web site in your browser. HTM-Elves can simply send the request for you.

For privileged operations, like creating a new repository on the GitHub site, you need to obtain a [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) that will be sent along with the request, to prove that the request comes from you and that you approve it.

To do this:

1. Log in to GitHub
2. Visit [the Personal access tokens (classic) page](https://github.com/settings/tokens)
3. Ensure that `Tokens (classic)` is selected
4. Click on Generate New Token

![Generate a new token](images/GenerateToken.webp)

5. In the pop-up dialog, choose Generate New Token (Classic)

![Choose token (classic)](images/ClassicToken.webp)

On the next page:

6. Add a note (like `HTM-Elves`) to remind you what this token is being used for
7. Set an expiration date. If you choose "No expiration", GitHub will "strongly [recommend] that you set an expiration date for your token to help keep your information secure". But it's your choice.
8. Check the `repo` button. This will give your token the authority to create new repositories for you, and to use gh-pages to publish them.
9. Ignore all the other operations
10. Scroll to the end and click on Generate Token

![Choose the settings for your token](images/SelectScopes.webp)

A new page will open with a long string of random numbers and letter that is your token.

![Copy your personal access token](images/CopyToken.webp)

11. Copy this string
12. In VS Code, in your `MyTutorials.github.io` folder, create a new file named `.env`.
13. Inside `.env` type `GITHUB_TOKEN=` and then paste the token, as shown in Figure 18 below.

![Create a `.env` file to store your personal access token](images/dotenv.webp)

<details class="note" open>
<summary>Keeping your secret safe</summary>
The `.gitignore` file in your `MyTutorials.github.io` folder contains an entry for `.env`:

```md-#
<i>node_modules/</i>
<b>.env</b>
<i>.DS_Store
.vscode/*</i>
```

This ensures that when you push your repository to GitHub, the `.env` file will not be sent to GitHub. Your secret token is safe.

</details>
<details class="pivot" open>
<summary>Access to the GitHub API</summary>
Now that you have a personal access token, and you have stored it in a place where HTM-Elves can find it, you can delegate most GitHub house-keeping tasks to HTM-Elves.

But before you can get HTM-Elves to work for you, you will need to install some Node modules that will be used by the `newTutorial.js` script, and by the `filter.js` and `watch.js` scripts inside the `public/` folder.

This is treated in the next step.

</details>
</section>