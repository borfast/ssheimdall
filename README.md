# SSHeimdall
An attempt at a centralized SSH key management tool


# Description

In Norse mythology, Heimdall (or Heimdallr, if you want to use the old Norse name) is the watchman of the gods. He dwelt at the entry to Asgard, where he guarded Bifrost, the rainbow bridge connecting Midgard to Asgard.

SSHeimdall is a play on the words "SSH" and "Heimdall".

I needed a simple way to manage SSH keys in multiple servers. There are many solutions available, like [KeyBox](http://sshkeybox.com/), [Userify](https://userify.com/), Ansible/Salt/Chef/Puppet, or using LDAP with SSH. None of those were good solutions, though: KeyBox could almost work but didn't fit my needs due to the way it works (I'll expand on that later), Userify is expensive, Ansible & co. feel wrong, are slow, and are not as flexible as I want (e.g. I also want to inspect the keys in a server), and finally, LDAP is way too complex for what I wanted.

Add to that the fact that I was looking for a little project to have fun with, and the answer was simple: I had to create my own SSH key manager.

And thus, SSHeimdall is born!


# Planned features

* Maintain a list of SSH keys SSHeimdall knows of.
* Allow adding, removing and creating new SSH keys via a web interface.
* Manage lists of servers that can be grouped together.
* List current SSH keys for each server and allow adding or removing keys.
* Manage profiles that consist of groups of SSH keys and can be applied to individual servers or groups.
* Multifactor authentication.
* Easy to use Docker image.
