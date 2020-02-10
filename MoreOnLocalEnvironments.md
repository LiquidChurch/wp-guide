# More on Local Environments

We offer a pretty opinioniated take on what to use for local development (VVV) and this is not the only option nor perhaps the most popular. This document attempts to briefly address alternatives and why VVV is recommended.

## Natively
One can run a WP stack on one's local machine. At first glance this can seem the easiest way forward but it has several significant disadvantages:
1. If you create a mess of your dev environment (we all do) you've also made a mess of your entire system.
2. Building the stack manually can be quite time consuming and prepackaged offerings are often quite slow.
3. You open your system up to security vulnerabilities by running server software directly on it.

Conclusion: Just don't do it.

## Docker
The favored child currently is Docker. It offers lighter weight "containers" than traditional Virtual Machine offerings and theoretically is a more attractive option BUT:
1. Docker is fairly easy to break.
2. In our experience environments built on Docker aren't quite as stable or full-featured as VVV.
3. It's a great tool that you probably don't need for this work.

Conclusion: Will get there but not quite yet. Expect configuration headaches.

## Virtual Machine
You could build out a virtual machine yourself, but why? VVV offers it pre-built.

Conclusion: Unless you really need to build a custom setup this is unnecessary.

## Hyper-V
Theoretically, you can use VVV with Hyper-V...the reality is you can't...or sometimes sporadically can...Its not a good situation. Just say no.

Hyper-V breaks other hypervisors so you can't even run VirtualBox, etc. alongside Hyper-V.

Conclusion: Just don't! And that includes using it as the provider for VVV, its a nightmare. Someday this will improve but it hasn't yet.

## Windows Subsystem for Linux (WSL)
Another attractive option for Windows users is WSL. Its light, contained, etc. But there isn't the sort of mature, pre-packaged deployment of the WP stack one finds in VVV.

Conclusion: There are limitations in WSL1 which undermine some of the advantages of a more virtualized system. WSL2 shows promise but wait for a more mature stack to develop.

## Vagrant / VVV
Vagrant runs a full virtual machine under the hood (usually via VirtualBox), so it isn't the lightest system out there, but its command structure is fairly simple, the system comes with a robust series of packages, and there is a significant community around VVV.

At some point in the future we expect that VVV/Vagrant will fully support Docker containers, if such should come about this may be a good option.

## Others
- Local by Flywheel is a nice system but they've decided to move it from Docker to native systems. Its still easy to use but concerns about security and messing up the entire computer are still valid.
- Devilbox works well but its default configuration is more complex than necessary.