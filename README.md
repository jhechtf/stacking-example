# Stacking Example

This is the stacking example repo. Code will be contributed to the repo in stacks of changes in order to show the workflow and any corresponding UIs

## Graphite

The Graphite CLI can be installed by running `brew install withgraphite/tap/graphite`, and then configuring Graphite with 
the `gt init` in the repo directory, as well as a following the instructions to authenticate the CLI given [here](https://graphite.dev/docs/install-the-cli#authenticate-the-cli).

One of the nice things about the `gt` CLI is that it has command pass through; if you attempt to call a command that isn't in `gt`, it will send that request to `git` instead. So running something like `gt add --help` is actually just a new shorthand for running `git add --help`.

### Branches / Starting a Stack

To create a new branch, you have a few options. These are shamelessly stolen from Graphite's own docs

```sh
# navigate to the trunk branch of your repository
gt trunk

# * build part 1 of your feature *

# the following two commands create a new branch off of main with your changes and add a commit

# add all unstaged changes (same syntax as git add)
gt add -A
# create a commit on a new branch with its name inferred from your commit message
gt create
# OR specify your commit message via an option, just like git
gt create -m "part 1"
# OR you can also specify a branch name yourself
gt create making_part_1
# This works too!
gt create -m "part 1" making_part_1


# If you don't run `add`, you'll be prompted to add your changes interactively.
# You can also run `add` as part of the create command with the `-a` flag
gt create -am "part 1"

# You can make the previous command even shorter by using an alias (most common gt commands have an alias, and you can even configure your own!)
gt c -am "part 1"
```

I'm partial to creating my own branches (e.g. `gt create graphite`), but whatever works for you.

To turn this single branch into a PR on GitHub, you can use the `gt submit` command.

<!-- DOWNSTACK: Add in info about creating other branches off of this branch -->

### Cool Commands

We're coming back to update the base PR with some cool commands we've found in Graphite

1. `gt checkout` - Every PR in a stack is just a different branch and can be checked out as normal. You can also use `gt switch` if that's more your speed.
2. `gt up` switches to the child of the current branch. Will prompt if ambiguous.
3. `gt down` switches to the parent of the current branch. Will prompt if ambiguous.
