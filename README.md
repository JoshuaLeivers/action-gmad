# action-gmad

GitHub Action to compile Garry's Mod addons into `.gma` files using `gmad`.


## Usage

Add the following to your GitHub Actions workflow:

```yml
...
  - uses: JoshuaLeivers/action-gmad@v1
    with:
      gma-name: my-cool-addon.gma
```

This will compile the addon in the repository with the specified name.
By default, the repository name will be used if a `gma-name` is not specified.

To access the `.gma` file in other parts of your workflow, use `actions/download-artifact`.
The file has the artifact name of `gma-file`.
