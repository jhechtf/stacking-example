# Stacking Example

This is the stacking example repo. Code will be contributed to the repo in stacks of changes in order to show the workflow and any corresponding UIs

## Git Town

Git Town is a set of utilities added into the base `git` command. As such, cloning a repo starts off very similar

```sh
git clone git@github.com:jhechtf/stacking-example.git
```

Once you have git town installed, you can run `git town config setup` to add in some aliases for convenience. Otherwise, you can run all commands mentioned by
using `git town [command name]`. For example, `git hack feature-1 #(with aliases)` becomes `git town hack feature-1`. To make it clear what is a git-town command,
I will be referencing them by the non-aliases version, though I do recommend installing it.

### First Branch / Starting a stack

To create this feature branch, run

```sh
git town hack git-town
```

Next we go through the usual process of `git add . && git commit -m "docs(README): Adds in basic instructions for git town"`

The next part is different, we're going to use 

```sh
git town sync
```

### Next Stack 

To get started on the next thing in the stack, create a new branch with `git town hack feat/town-add-basic-rust-pkg`. This automatically creates a new branch and tracks that branches parent.

Then you'll run `cargo init && cargo run` to verify that the application compiles and that you see `hello world` printed out in your console.

Let's go ahead and add things in like we normally would --

```sh
git add .
git commit -m "feat: Adds in basic Rust application"

```

