<!-- Tutorial Repository on Github -->
<section
id="tutorial-repository-on-github"
aria-labelledby="tutorial-repository-on-github"
data-item="9. Tutorial Repo on Github"
>
<h2><a href="#tutorial-repository-on-github">Create a Tutorial Repository on Github</a></h2>

To share your tutorial online, you will need to create a remote repository on GitHub. HTM-Elves expects you to use exactly the same name for your remote repository as for the tutorial directory that you just created.

The directory that was just created is called "Demo". If you look inside the file at `Demo/docs/md/99-Introduction.md`, you will see that it starts something like this:

```yaml
---
title: Demo Tutorial
subtitle: (replace with your own content)
month: December 2024
organization: MyTutorials
repo: Demo
---
```

Pandoc will use the entries for `organization` and `repo` (which "Demo" in this case) to generate the links that you can find at the foot of the menu.

![The link to your GitHub repository is created automatically](images/GitHubLink.webp)

So now you need to create a GitHub repository at this location.

1. In your browser, visit the home page of your tutorials Organization.
2. Click on the Repositories tab
3. Click on the green New Repository button

![Creating a new repository](images/NewRepo.webp)

4. On the next page, check that the Owner of the repository is indeed your new tutorials organization, and give your new repository the name Demo.
5. Ensure that the Public radio button is checked
6. You can leave the other fields as they are
7. Click on the Create Repository.

![Naming your new repository](images/NameRepository.webp)

8. On the next page, scroll to the end and copy the last three commands, as shown in Figure 20 below.

![Copy the commands to set the remote for your local repository](images/AddOrigin.png)

9. Back in VS Code, open a Terminal window on the Demo directory, and paste these commands. Use Ctrl-Shift-V (or Command-V on a Mac).
10. Press Enter, to execute.

![Add the remote origin, and push your last commit](images/AddRemote.webp)

<details
class="tip"
open
>
<summary>Creating a GitHub Repository Automatically</summary>
As you might have guessed, the HTM-Elves workflow does provide a way for you to automatically create a GitHub repository, and to push your initial commit to it, with no input from you.

However, before this will work, you will need to create a GitHub authorization token, and this requires some extra steps. I've described the process for doing this in the [Writing Your Own Tutorials](https://htm-elves.github.io/Writing-Your-Own-Tutorials/#automatic-repo-creation) article.

</details>


</details>
<details
class="pivot"
  open
>
<summary>Ready to go online</summary>
Now that you have set up a GitHub repository for your Demo tutorial repository, when you click on the links at the foot of the menu, your browser should take you to the GitHub repository page, or to the Issues section if you click on Feedback.

After one last step, you will be able to share this tutorial-that-you-did-not-write with the world.

</details>
</section>