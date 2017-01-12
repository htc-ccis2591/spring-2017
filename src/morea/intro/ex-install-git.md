---
title: "Install Git"
published: true
morea_id: install-git
morea_type: experience
morea_summary: "How to install git on Windows through GitHub Desktop, and check for and install git (if needed) on a Mac."
morea_sort_order: 2
---

# Install Git
The install process for git is different based on the type of computer you are using.  Install information is provided here for Windows & Mac OS.  If you are using Linux, it is likely that you already have git and if not can use the package manager to easily install it.

## Windows Users
If you are a Windows user, typically you will use PowerShell as your command shell.  However, Windows PowerShell does not include git by default.  You will need to download and install git from the web. You can get it from the [Git-SCM Downloads](https://git-scm.com/download/win).

I recommend that you keep the default install settings suggested by the installer, specifically:
<div class="row">
<div class="col-md-6">
<img class="img-responsive" src="{{ "/morea/intro/images/git-install-opt1.png" | prepend:site.baseurl }}" alt="Screenshot of install options">
</div><div class="col-md-6">
<img class="img-responsive" src="{{ "/morea/intro/images/git-install-opt2.png" | prepend:site.baseurl }}" alt="Screenshot of install options">
</div>
</div>

<br>
This will install a few different options that allow you to work with Git on a Windows computer.  You may choose any of them you like, but I would recommend GitBash as it will be closest to what you may see from my examples.

## Mac Users
If you are using a Mac, open up a [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) window and type git.  You may find that it is already installed, or if not that it will prompt you to install the XCode Command Line Developer Tools.  If it does not, you likely have an older version of the Mac OS and should download and install the tools from the [Apple Developer Site](https://developer.apple.com/downloads/index.action).  You can also install the full XCode suite from the Apple App Store, but this will take additional space.  

GitHub Desktop is not required, we only need the underlying git command, and actually I encourage you not to use the application itself, but there is also now a [GitHub Desktop for Mac](https://desktop.github.com/)

## Configure Git
Before you dive in, you'll want to configure git with your user information. In the commands below, fill in your GitHub name and the email used with your GitHub account.  The email address is what will tie your activity to your account.  **Make sure that you are using the same email and check for typos.**

### Config for Public (Shared) Computer
Use this only for a computer which is public or shared.  This configuration is applied only to the current git repository directory.  It must be repeated for each repository you clone or create.  
{% highlight bash %}
$ git config user.name "User Name"
$ git config user.email "user@email"
{% endhighlight %}

I also recommend saving this git config customized with your information as a Gist on GitHub so that it is easily available for you to use on any computer.

### Config for Personal (Home) Computer
Use this only for a computer where you are the only GitHub user.  
{% highlight bash %}
$ git config --global user.name "User Name"
$ git config --global user.email "user@email"
{% endhighlight %}
