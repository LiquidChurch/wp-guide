# Version Control Using Git

You should be using [GitHub](https://github.com/) for your code repositories and [Git](https://git-scm.com/) as your client/local repository host. Feel free to utilize a GUI based interface on top of the git software if you prefer (most IDE's have some support built-in).

## Git on Windows
Using Git is smooth sailing on Windows UNLESS you need to authenticate with SSH. While the latest versions of Windows do include an optional OpenSSH client this version tends to lag behind the current release significantly and there are significant difficulties in using it.

You can avoid these headaches by using Git either within Git Bash or within VVV.

## Create/Clone Repositories
- If you are starting a new project from scratch you'll want to create a repo on GitHub and clone that repo down to your local machine.
- If you are working on an existing repo you'll clone it to your local machine.
- You should clone into: vvv/www/wordpress-one/public_html/wp-content/{plugins-or-themes}
    - By default the github repo name will be used as the folder name.

## Troubleshooting
- See [Error: Agent Admitted Failure to Sign](https://help.github.com/en/github/authenticating-to-github/error-agent-admitted-failure-to-sign) for issues with SSH.

## Footnotes
[^1]: One could also run these commands through WSL, but in our experience WSLv1 and WSLv2 both could use a bit more refinement before they become optimal tools for WP dev use.