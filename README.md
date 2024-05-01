# Stacking Example

This is the stacking example repo. Code will be contributed to the repo in stacks of changes in order to show the workflow and any corresponding UIs

## Sapling

Sapling is actually an entirely different Source Control than Git, but it does interoperate with Git. This means that even though
this repo is a Git-based repo, I created the copy of it on my machine wite `sl clone git@github.com:jhechtf/stacking-example.git`

This is useful because as far as I am aware, Sapling doesn't have its own hosting platform available. 

To create the commit, run 

```sh
sl commit -m "docs(README): Adding in basic docs for Sapling usage"
```

Then, to push up the stack run 

```sh
sl pr submit
```