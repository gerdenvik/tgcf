Hopefully, you have already read the README for a basic introduction to `tgcf`.

The Termux app in Android offers you a full-blown Linux terminal.

[![image](https://user-images.githubusercontent.com/66209958/196798588-a05dc7ac-8dae-4fd1-8030-d790c63af682.png)](https://f-droid.org/en/packages/com.termux/)

Install the latest version of Termux from Fdroid. [Link](https://f-droid.org/en/packages/com.termux/)

## Install `tgcf` on termux

Just open your termux and run the following commands:

```shell
termux-info
pkg upgrade -o Dpkg::Options::="--force-confnew" --force-yes -y
pkg install libjpeg-turbo python micro -y
pip install --upgrade pip wheel setuptools
pip install --upgrade tgcf
tgcf --version
tgcf --help
```


## Testing

To test if `tgcf` was properly installed, 

```shell
tgcf --version
```

It should output version no. and that should match with the version of the [latest release](https://github.com/aahnik/tgcf/releases). 

## Configure and run

Learn about 
   - [environment variables](https://github.com/aahnik/tgcf/wiki/Environment-Variables), 
   - [CLI usage](https://github.com/aahnik/tgcf/wiki/CLI-Usage) and 
   - how to [configure tgcf](https://github.com/aahnik/tgcf/wiki/How-to-configure-tgcf-%3F), 
   and then start using `tgcf`.

When you install `tgcf` using the above method, the text editor `micro` is also installed. You can use `micro` to edit text files.



