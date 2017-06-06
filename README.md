# ansible-module-gitupdater

```
> GITUPDATER    (gitupdater.py)

  gitup https://github.com/earwig/git-repo-updater is a console script that allows you to easily update multiple git repositories at once.

Options (= is mandatory):

= path
        Full path to the git repository.
        (Choices: )[Default: []]
        version_added: 1.0
- state
        State of the gitup configuration for this repository. The git repository itself is not affected.
        (Choices: present, absent)[Default: present]
        version_added: 1.0

EXAMPLES:


# Bookmark a repository, state can be omitted
- gitupdater:
    path: /var/repos/project

# Bookmark a repository
- gitupdater:
    path: /var/repos/project
    state: present

# Delete bookmark
- gitupdater:
    path: /var/repos/project
    state: absent


MAINTAINERS: Josef Friedrich (@Josef-Friedrich)

METADATA:
	Status: ['preview']
	Supported_by: community
```

# Development

## Test functionality

```
/usr/local/src/ansible/hacking/test-module -m gitupdater.py -a
```

## Test documentation

```
source hacking/env-setup
/usr/local/src/ansible/test/sanity/validate-modules/validate-modules --arg-spec --warnings gitupdater.py
```

## Generate documentation

```
ansible-doc -M . gitupdater
```
