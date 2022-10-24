An environment variable is a dynamic-named value that can affect the way running processes will behave on a computer. They are part of the environment in which a process runs.

## All env vars

| Env Var          | Value                                                        | Requirement                                                  |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **`PASSWORD`**     | Password to protect access to web interface    | always required, defaults to `tgcf` if not provided                                              |





## Setting env vars

There are various methods to set env vars

### `.env` File

You can easily set environment variables for `tgcf` using a `.env` file in the directory from which `tgcf` is invoked.

```shell
PASSWORD=mypass
# put your real values here
```

### Cloud Deploys

When you are deploying to a cloud platform, and you cant create files (Heroku or digital ocean apps), you can set environment variables using the GUI provided by the platforms. Please read platform-specific guides in the wiki for more details.
