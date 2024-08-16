## Hugo Go Modules

One way to share parts of a Hugo sites between different projects is using [Hugo
modules](https://gohugo.io/hugo-modules/). 

Read more: 

- [Using Hugo Modules Instead of Git Submodules](https://www.adamormsby.com/posts/012-hugo-modules/)

## Initialize the project as a Hugo module

Before starting using Hugo modules in a new Hugo project you must first
initialize the project as a Hugo module. 

Check if you already have Go installed: 

```
go version
```

If you don't have Go installed, [download and install
Go](https://go.dev/doc/install). 

Next, [initialize the project as a Hugo Module](https://gohugo.io/commands/hugo_mod_init/):

```
hugo mod init foo
```

Here I use `foo` as the module path but any string seems to work. This will
create the [go.mod](https://go.dev/doc/modules/gomod-ref) file. 

## Resolve Hugo module dependencies

Now, to get references to the latest version of each module and save these in 'go.mod':

```
hugo mod get
```

Leep in mind that the stored module references in `go.mod`` are references to a
specific commit on a github repo, not a branch. 

## Theme Relearn

Once you have created the `go.mod` file you can add a Hugo theme as a Hugo
module instead of including the theme as a git submodule.

In the `hugo.toml` I can now add the Hugo Relearn theme as as Hugo module. 

```
[module]
  [[module.imports]]
    path = "github.com/McShelby/hugo-theme-relearn"
```

At the time of writing, this will use the version `5.27.0 (2024-04-07)` of the Relearn 
Hugo theme. 

If you add this to `hugo.toml` before initializing the project as a Hugo module
you will get an error. 

## Permission denied errors with the Relearn theme

With the `5.27.0 (2024-04-07)` version of the Relearn Hugo theme I can only
run Hugo with the  `-–renderToMemory` flag, otherwise I get permission denied
errors. 

- [Hugo forum discussion](https://discourse.gohugo.io/t/can-only-run-hugo-with-rendertomemory-otherwise-gets-permission-denied-errors-even-after-chmod-a-rwx/49335)  
- [GitHub issue 831](https://github.com/McShelby/hugo-theme-relearn/issues/831)
  - After reading the [issues
linked](https://github.com/McShelby/hugo-theme-relearn/issues/831#issuecomment-2061733009)
by [jmooring](https://github.com/jmooring):

    -  I've tried running ` hugo --noChmod `
but I still get the same permission errors.  

    -  But, setting `themeVariantModifier = ".gen"` in the `[params]` section in `hugo.toml` as described in the theme [Configuration](https://mcshelby.github.io/hugo-theme-relearn/basics/configuration/index.html#annotated-config-options) section of the theme Relearn documentation  worked fine.  I'm happy this workaround exists but at the same time appreciate that the  root cause will  be fixed in the next release of the Relearn theme. 

## Make and test changes in a module

One way to do local development of a module imported in a project is to add a
replace directive to a local directory with the source in `go.mod` as described
[here](https://gohugo.io/hugo-modules/use-modules/#make-and-test-changes-in-a-module).

Instead of modifying the `go.mod` files, you can also use the modules
configuration replacements option as described [here](https://gohugo.io/hugo-modules/configuration/#module-configuration-top-level).


## Update modules

To update all modules in a project:

```
hugo mod get -u
```

This will update `mod.go` with referenses to the latest version of each module. 

Read more
[here](https://gohugo.io/hugo-modules/use-modules/#make-and-test-changes-in-a-module)
about how to update a specific module and more options. 

## Multiple Hugo sites

All material specific to a year is found inside the directory with name of the year. 

For each year there is one swedish Hugo site and one english Hugo site. For example, for
the year 2024, the swedish site is in the `2024` directory and the english site in
the `2024/eng` directory. 

Each site has its own `hugo.toml` configuration. To build a specific site, use
`hugo` with
the 
`--config` option to select the site configuration. 

For example, this is how to
build the swedish 2024 site. 

```
hugo server --config=2024/hugo.toml
```

And this is how you build the 2024 english site. 

```
hugo server --config=2024/eng/hugo.toml
```

## Deploy to GitHub pages


Configuration file: `.github/workflows/hugo.yaml`