halias: A HOSTALIAS Manager
===========================

halias manages HOSTALIASES files, so you can have separate namespaces for
different tasks.

For example, you might have www as an alias for your home webserver at home and your works intranet when at work.

Usage
-----

halias add|create|current||list|remove|use [args]

Args:
* add: alias hostname
* create: file
* remove: alias
* show: file (optional)
* use: file

Commands:
add: Add an alias to the curren file
create: Creates a new file and switches to it
current: Show the currently active file
list: List the available files
remove: Remove an alias from the curren file
show: Show the contents of the given file (or the current one if no args given)
use: Switch to the specified file

Files are kept in /home/psa/.hostaliases.d

To use the aliases, you need to put the following line in your
.profile or .bash_profile (and run it for current terminals):
export HOSTALIASES=/home/psa/.hostaliases

Examples
--------

Add www to point to your company intranet:

```halias add www intranet.example.com```

Remove www from your aliases file:

```halias remove www```

Create an empty home profile and add www to it:

```
halias use home
halias add www cassowary.example.org
```

List the current configurations available

```halias list```
