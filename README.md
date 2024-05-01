# Stacking Example

This is the stacking example repo. Code will be contributed to the repo in stacks of changes in order to show the workflow and any corresponding UIs

## Sapling

Sapling is actually an entirely different Source Control than Git, but it does interoperate with Git. This means that even though
this repo is a Git-based repo, I created the copy of it on my machine wite `sl clone git@github.com:jhechtf/stacking-example.git`

This is useful because as far as I am aware, Sapling doesn't have its own hosting platform available. 

For the base commit, we needed to create a new named "branch", though Sapling calls them "bookmarks." This is done with

```sh
sl book sapling
```

To create the commit, run 

```sh
sl commit -m "docs(README): Adding in basic docs for Sapling usage"
```

Then, to push up the stack run 

```sh
sl pr submit
```

### Next Commit

Instead of explicitly telling Sapling we're making something new, we simply run

```sh
# Initializes the basic rust repo
cargo init
# Adds items to be tracked by sapling
sl add
# Adds commit message
sl commit -m "feat: Adds basic Rust project"
# Updates the stack
sl pr submit --stack
```

