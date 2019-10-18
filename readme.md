Commando - A Simple Guide to the Linux/OSX Command Line
========

Have you ever sat at your computer, hopelessly googling for linux commands? Yes, yes you have. And don't worry, I have too. In fact, I did this so much that I just started taking notes for myself. Turns out this list is quite useful now, so I thought I'd share it. 

Commando aims to be a simple guide to the Linux command line. It's not quite there yet, as this is just my notes but send me some pull requests and hopefully we can get there. As is, I think this thing is pretty useful - at least to me. Hopefully you find it useful too.


Index of Commands
-----

So far, I have the following breakdowns of commands:
* [Command Line Basics](basics.md)
* [Ansible w/ Vagrant](ansible.md)
* [AWS - just cert replacement](aws.md)
* [Docker, early yet](docker.md)
* [Front-end Tooling, general stuff](front-end.md)
* [Git](git.md)
* [Heroku, deployment](heroku.md)
* [Homebrew (Mac package manager)](homebrew.md)
* [Lando, Docker-based local dev + setup](lando.md)
* [Linux/Ubuntu](linux.md)
* [MongoDB w/ setup commands + DB commands](mongodb.md)
* [MySQL](mysql.md)
* [Python + PIP](python.md)
* [Shopify, theming mostly](shopify.md)
* [Terminus, from Pantheon](terminus-pantheon.md)
* [Transfer protocols (SFTP, SCP and rsync)](transfer.md)
* [Vim](vim.md)

Yeah, there is some overlap here but nothing big. If you have questions, hit me up via github and I'm sure we can sort it out.


What Does This Repo Do?
-----

This is an educational resource and reference point for all the fun you will have on the command line. Taken as a whole, it doesnt do much. But if you have a modern web project, my guess is you're going to need these commands.


What Do I Need to Use This?
-----

You are going to need a text editor and a terminal. I like Sublime Text and iTerm2 terminal on the Mac and in Ubuntu, I use the included Vim text editor and the Guake terminal.

Links to the Goods:
* [Sublime Text](http://www.sublimetext.com/2)
* [iTerm2](http://www.iterm2.com)
* [Guake](https://apps.ubuntu.com/cat/applications/precise/guake/)

OSX has a unix-like core, so most of the commands on Linux work for OSX. There are some deviations, noted where appropriate in the command reference docs.


How Can I Contribute?
-----

Believe it or not, you probably know the command line much better than I do. And I'd love to have your additions to this repo, if for no other reason than the fact I could use more reference. If you have extra commands to add to the existing files, continue to use the format I have established:

Any variable you use in a path (like a username or password) should be laid out like this:

```
your-password-here
your-username-here
your-whatever-here, etc
```

If you want to add a whole new section, do it! I'd just ask that you put it into a new file as a pull request so we can get a bird's-eye view of what's going on in this repo. There pretty much isnt any pull request I'm going to deny - shoot away.


Obligatory Arnold Shot from Commando
-----

![Arnold in Action, Commando Movie](img/arnold-in-action.jpg "Arnold in Action, Commando Movie")


Thanks
-----

* To you Mr. Internet, where we would be without each other?
* [Google](http://google.com), I can't even imagine the command line before you existed.
* [Superuser.com](http://superuser.com), part of the Stack Overflow network. A great resource for command line questions.
* And especially to [Sarah Thrasher](https://github.com/sarahjean), who has taught me so much about this mysterious black box, the command line.