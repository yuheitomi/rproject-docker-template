# How to set up

Before building and launching the container based on this template, create cache directories for `renv` and `pak`, as well as RStudio config directory.

```sh
$ mkdir ~/.cache/R/renv # renv
$ mkdir ~/.cache/R/pkgcache # pak
$ mkdir ~/.config/rstudio-server # rstudio configs
```

In the `Dockerfile`, several cache and configuration directories are created under `/home/rstudio/` with user's priviledge.

## Environmental variables

- `ROOT` is true to enable `sudo` command in RStudio terminal. Password is `password`.
- No authentication is required to log in to RStudio Server.
- `RENV_CONFIG_PAK_ENABLED` is set true to enable `pak` by default for `renv`.
