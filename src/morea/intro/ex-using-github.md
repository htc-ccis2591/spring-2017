---
title: "Git & GitHub: Update the Student Directory"
published: true
morea_id: using-github
morea_type: experience
morea_summary: "Practice using the shell, git and GitHub to get, create, update and manage files."
morea_sort_order: 3
---

# Practice using Git and GitHub
If you do not already have a [GitHub](https://github.com/) account, please visit the website to register for a free public account now.  If you use your student email, you can later request a free Personal account upgrade through the GitHub [Student Developer Pack](https://education.github.com/pack).

## Prerequisites
The following topics were covered earlier:

- [Install Git]( {{ site.baseurl }}/morea/intro/ex-install-git.html ): To complete this exercise, you need to have git installed.  
- [Install, Configure, and Use Brackets]( {{ site.baseurl }}/morea/intro/ex-install-brackets.html ): You should use Brackets to edit the files.  
- [Shell Basics]( {{ site.baseurl }}/morea/intro/read-shell-basics.html ): I will assume that you know how to access the appropriate shell for your OS that is able to execute git commands.


## GitHub Assignment Workflow

1. Most assignments will begin with a starter repository that you will *__fork__*.  This gives you a general layout for the project and any starter code that you should have to begin.  
2. You'll then *__clone__* the repository to your computer, this gets you the files to edit.
3. Add or edit files to make changes and then *__add__* to the staged version.
4. Then you *__commit__* the version to your local repository.  It's a good habit to commit code locally (on your computer) often.  This allows you to make specific notes on what you've done in the commit messages, and gives you a point to go back to if you want to undo something.  
4. When you're done with a chunk of work, or just need to save it *in the cloud* to go home for the night, you *__push__* your changes up to GitHub.  
5. (Optional) To get those changes on another computer where the files have already been cloned, you *__pull__* them.  
6. When you are done with the assignment and are ready to submit it for grading, you make a *__pull request__*.  This allows me to give you in-code feedback as I  grade.   

Let's walk through this workflow on the student directory project.  

{% include alert.html type="danger"
    content="The video and images below walkthrough this process for the HTML organization.  The repository urls and organization name will vary for this course.  Please use the links provided in step 1 below to access the correct organization and repository.  Don't try to type it in from the video or screenshots." %}

{%  include youtube-small.html  id="ESzwfyVeqsg" %}


### Fork
First you'll get your own copy of the repository, this called "forking". A fork is your own personal copy of code.  You can modify it in any way you like, and it does not affect the person you copied it from.  However it does maintain a link, which we'll discuss later.

1. Go to our [{{ site.github_org_name }}]({{ site.github_org_url }}).  You'll notice there is a repository there called [js-students]({{ site.github_org_url }}/js-students).  

2. Click the link to go to the repository page, then click the icon in the upper right corner to *fork* the repository to your account.  
  <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_fork.png" alt="GitHub page snippet showing the location of the fork button.">

3. Now go to your GitHub page and you should see students under your repositories.  This is a copy of the repository from our class organization.  You can see the note that says it is forked.  That let's you know that it is a copy.
  <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_forked_students.png" alt="GitHub page snippet showing forked repository on personal account.">

4. This is *your* copy.  The changes you make here are only visible to you.  They are not made in the original class repository.  


### Clone
Now you need to get the repository onto your computer so that you can work with it.  This is called "cloning".  

<div class="alert alert-danger" role="alert">
When you clone a repository for class, it is important that you do it from your fork of that repository. Look for your user id before the repository name in the clone URL. If you clone the class repository you will not be able to push up your changes.
</div>

1. Click on the html-students link to go to the repository page.

2. Copy the URL from the repository page.  
  <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_clone_url.png" alt="GitHub page snippet showing the location of the clone url.">

3. Next we leave the browser and go to the shell and go to the location where you want the repository to be pulled down. (Use the `cd` command to change your directory.)

4. Use the `git clone` command to get a local copy. <br>`$ git clone <paste-clone-url-here>`

5. Use the `ls` command to list the files/directories, and should now see a new html-students directory in that location.

6. When working with a git repository, you need to be inside the repository directory.  Use the `cd` (change directory) command to go into the html-students directory.  


###  Make Changes
Now that you have a personal copy of the student directory, you can make changes to the project files.  Use [Brackets](http://brackets.io/) to add a new file as indicated below.  

1. In the html-students directory.  You should see an _data directory with a subdirectory for the current semester.  

2. Locate my *mbmosman.yml* file.  This is a[YAML](http://www.yaml.org/start.html) file, a format based on key/value pairs separated by a colon (:).

3. Make a copy of the file and rename to *your* GitHub user name with the .yml extension.

4. Open the file in Brackets and update the contents to have your name, a custom emoji, and a short introduction.  Here's a list of the [emoji](http://www.emoji-cheat-sheet.com/) you can use.  Be careful with the formatting. Do not put colons around the emoji name.

5. In most cases, you'd now test to make sure things look OK.  While you could test this locally, there's some extra set up needed for this type of Jekyll GitHub Pages site.  (Look it up later if you are curious.  This is how the course web site is built too.)  We'll skip the testing locally and just commit our change, but you might need to come back later and fix it if you weren't careful.

6. Go back to the shell and use the <code>git status</code> command to see what changes you have made.<br><code>$ git status</code>

7. You should see that you've got an untracked file.  Use the <code>git add</code> command to add your file.  You can append the file name to the command to add a single file, or you can add a . to add all the new files at once.<br><code>$ git add &lt;your-file-name-here&gt;</code><br>OR<br><code>$ git add .</code>

8. Use git status to verify that you're file has been added.  

9. Now it's time to commit the change.  This will version your change in your local git repository.  Use the <code>git commit</code> command.<br><code>$ git commit -m "Your message about the change here."</code>

10.  It's good to commit small groups of changes with specific messages.

### Push Changes
To get your changes from your local repository to the GitHub repository you do a push.

1. Before you push your changes, you should check that the branch you are on matches the remote branch you want to push to. It will often be master in the real world, but for our class assignments, which we want GitHub to host for us, it will be gh-pages.  You can see which branch you are working on by using the <code>git branch</code> command.

2. If your local and remote branches match, then you can just say `git push` and everything should go up to GitHub.

3. If your local and remote branches are different, then you need to say which remote branch you want to push to:<br>`$ git push origin <remote-branch-here>`

4.  Check the GitHub repository page in the browser to make sure you got the changes up successfully.  
  <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_pushed_changes.jpg" alt="GitHub page snippet showing the time of the last update.">

### Test!
Before asking to merge your changes back into the class repository you should make sure you didn't break anything.  In GitHub, if you click on the Settings tab for your html-students repository, you should see highlighted in green a URL where your page is published.
<img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_test_changes.png" alt="GitHub Settings page snippet showing the location of the publish URL.">

When you click the URL, you should see the Student Directory page click the link for your semester and you should see both my information and yours.  
<img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_test_page.png" alt="Student Directory page snippet.">

If the page is not coming up, double check the syntax and naming of your .yml file.  If you are not seeing your picture or icon, then your file name is not the same as your GitHub user id.  


### Pull Request
Once you have working changes on your repository & web page, you want to submit a pull request for the source repository (our course organization) to merge those changes.  This is the last - but most important - step, the one that turns in your assignment.

1. From your repository page, click the Pull Request button.  
  <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/github_pullreq_tab.png" alt="GitHub page snippet showing the pull request button.">

2. The next screen will show you all the changes between your copy of the repository and the original.  Review the changes, then click the green button to create the request.

4. The next page allows you to enter a commit message and (optionally) comments for the reviewer. Click the green button again to open the request.

5. Make sure to verify that you see the green button that says your pull-request is open, and do not close it.  I will not see or grade requests that are closed.


## Submit Work for Grading
There are 3 things to submit into the dropbox for this.
Your pull-request on GitHub is one part of your submission for this assignment.  In addition to creating the pull request, you also want to submit the following items into the Module 1 Assignments box on D2L.

1. GitHub Student Directory live web page screenshot
    <div style="padding:10px 20px">
      <div class="row"><div class="col-sm-6">
        Sample Screenshot:
        <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/pull-req-screenshot-sample.png" alt="A sample screenshot of the pull-request">
      </div></div>
    </div>
2. GitHub Student Directory pull request screenshot
    <div style="padding:10px 20px">
      <div class="row"><div class="col-sm-6">
          Sample Screenshot:
          <img class="img-responsive" src="{{ site.baseurl }}/morea/intro/github-demo/page-test-screenshot-sample.png" alt="A sample screenshot of the web page">
      </div></div>
    </div>

You can take a screenshot on most windows computers by looking for the PrtSc or PrtScn button on your keyboard.  That will screenshot the entire desktop.  If you use Alt + PrtScn that will screenshot the active window.  This puts the screenshot in the clipboard.  You will need to paste this into a MS Word document to save and submit it.

On Mac, you can take a screenshot by using the command+shift+4 key combination.  This will allow you to select the area on the screen to screenshot.  If you hit the space key, it will change to highlight the active window for the screenshot.  Click the mouse to take the screenshot and it should save to your desktop.
