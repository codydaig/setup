# Windows Subsystem for Linux

Windows Subsystem for Linux \(WSL2\) makes life significantly easier for people who want to use and develop open source projects on Windows, but requires that you keep a few things in mind.

1. Understand the difference between installing/running applications on WSL2 vs Windows 10.
2. To avoid huge wastes of time, don't modify the default shell that WSL2 comes with (Ubuntu Bash) to `zsh`, `fsh`, `ksh`, etc. \(If you don't know what this means, don't worry about it!\)

## Applications on WSL2 vs Windows 10

At this point, you might already have Git and Node.js installed on your regular Windows 10 setup. While this works great for basic use cases, we'll want to use Linux Bash exclusively for command-line based applications \(like `git` and `node`\) because:

1. WSL2 will have fewer problems running these applications \(more on that [here](https://docs.microsoft.com/en-us/windows/wsl/faq#why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows)\).
2. Having applications installed on both WSL2 _**and**_ Windows 10 will be confusing and hard to keep updated.

### Install before Day 1

Here's a table that shows which software should be installed in which environments before W1D1:

| Application | Environment |
| :--- | :--- |
| [Sublime Text 3](https://www.sublimetext.com/3) | Windows 10 only |
| [Visual Studio Code](https://code.visualstudio.com/Download) | Windows 10 only |
| [Zoom](https://zoom.us/download#client_4meeting) | Windows 10 only |
| [Slack](https://slack.com/downloads/) \(note 1\) | Windows 10 only |
| Git \(note 2\) | Ubuntu Bash only |
| Node.js via [nvm](https://github.com/creationix/nvm#install-script) \(note 3\) | Ubuntu Bash only |

\(Note 1\) Students who don't install the standalone Slack desktop application usually have trouble keeping up with the course, so please make sure you install it.

\(Note 2\) Git should already be installed on Ubuntu Bash. If you don't get an output for `git --version`, then run `sudo apt install git`.

\(Note 3\) One of the most reliable ways to install Node.js is via `nvm`, **not** via`apt install`. First, install `nvm` by running either of the [install scripts](https://github.com/creationix/nvm#install-script) via Ubuntu Bash. Then, run `nvm install --lts` to install the latest "Long Term Stable" \(LTS\) version of Node.js, **not** the "Current" version of Node.js. You should now be able to run `which node`, which will indicate that your `node` command is installed in the `~/.nvm` directory.

### Install after Day 1

Below is a preview of some software that you may be installing and using after the first day of class. Don't bother looking into any of these things now, except to remove any previous installations of MySQL and MongoDB from your regular Windows 10 setup.

| Application | Notes | Environment |
| :--- | :--- | :--- |
| MySQL \(note 1\) | v5.7 \(not v8\) | Ubuntu Bash only |
| MongoDB |  | Ubuntu Bash only |
| [React](https://reactjs.org/) |  | via `npm` or `npx` only |
| [Webpack](https://webpack.js.org/) |  | via `npm` or `npx` only |
| [nodemon](https://github.com/remy/nodemon) |  | via `npm` or `npx` only |

\(note 1\) Some people may run into issues installing and running MySQL or MongoDB. Microsoft has outlines how to install the supported versions onto WSL2 [here](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-database). With MySQL installation issues, [installing the equivalent version of MariaDB instead](https://mariadb.com/kb/en/library/mariadb-vs-mysql-compatibility/#drop-in-replacement-for-mysql) is a great alternative.

## Working with Files on WSL2

Microsoft has changed the way to work with files in WSL1 vs WSL2. In WSL2, the easiest way to consistently work with files on your Linux machine from windows applications is by mapping a network drive. Go to This PC -> Map a Network Drive -> Choose a letter of your choice and put `\\wsl$\Ubuntu-20.04` as the network path and click mount. Now when in VS Code or other applications you can choose the network drive from the File Explorer and navigate to your home directory `/home/username/`. Almost everything you do initially should be from within your home directory on Ubuntu Bash. This is where you will clone your git repos, create new projects, and much more! 
