DigitalOcean infrastructure is a leading cloud service provider based in the United States of America. Their headquarter operates from New York City, and their data centers are prevalent in every corner of the world in order to provide seamless cloud services across the globe.

<details>
<summary>App Platform</summary>


![create-app](https://user-images.githubusercontent.com/66209958/113475188-aab3a200-9491-11eb-8649-9c4111d05a1b.png)

Click **Create** -> *Apps*


![source-is-docker-hub](https://user-images.githubusercontent.com/66209958/113475207-c1f28f80-9491-11eb-84d1-5b90e6a4ee3c.png)

Choose **Docker Hub** as the source.
Choose the **type** as _"Web"_

In the next step,the **repository** path is _"aahnik/tgcf"_.

You can now set the values of the [environment variables](https://github.com/aahnik/tgcf/wiki/Environment-Variables) from this beautiful interface provided by Digital Ocean.


Give any name to your app. After this, you will be lead to a pricing page. Choose a pricing plan suitable for you and click "Launch basic app".
</details>


<details>
<summary>Ubuntu Droplet</summary>

If you want more control, you may run `tgcf` on a VPS like DigitalOcean's ubuntu droplets.

Steps:
Create a Droplet and SSH into it using Termius App or Open Console in Browser. Then in your terminal execute the following commands.

1. Update packages and reboot
```shell
sudo apt update && sudo apt upgrade -y
reboot
```
2. Reconnect and install dependencies
```shell
sudo apt install python3-pip python3-venv
``` 

3. Follow the steps as shown in README to install and run tgcf.
4. Closing the console stops the running `tgcf-web` process. You can use a detached screen session to keep tgcf running in background.
```shell
# make sure you are inside your my-tgcf directory
screen -S tgcfSession
source .venv/bin/activate
tgcf-web
```
Exit the screen session by <kbd>Ctrl</kbd> + <kbd>a</kbd> then press <kbd>d</kbd>.
Now you can safely close the console to VPS.
</details>

