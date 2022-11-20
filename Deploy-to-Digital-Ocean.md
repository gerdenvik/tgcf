DigitalOcean infrastructure is a leading cloud service provider based in the United States of America. Their headquarter operates from New York City, and their data centers are prevalent in every corner of the world in order to provide seamless cloud services across the globe.

<details>
<summary>App Platform</summary>
<br>

1. Click **Create** -> *Apps*

    ![create-app](https://user-images.githubusercontent.com/66209958/113475188-aab3a200-9491-11eb-8649-9c4111d05a1b.png)



2. Choose **Docker Hub** as the source. **repository** path is _"aahnik/tgcf"_. Click "Next".

    ![select-docker-hub](https://user-images.githubusercontent.com/66209958/202895433-88320c4b-67cc-46e5-8bcf-905b53808c9a.png)

3. A page will appear where you can edit your app resources. (Zoom and understand the image)

    ![app-resources](https://user-images.githubusercontent.com/66209958/202896017-7a51b267-0f4b-4281-9b55-be4ed4142cc4.svg)

4. Set your [environment variables](https://github.com/aahnik/tgcf/wiki/Environment-Variables).

    ![set-env-vars](https://user-images.githubusercontent.com/66209958/202895453-e7589b7f-1bea-44c1-acb8-19f5eb489e45.png)

5. Choose your location

    ![choose-region](https://user-images.githubusercontent.com/66209958/202895459-4853c750-8e85-4d13-a329-a7c62a7ed9e6.png)

5. Wait for the deployment to be done. Once done click on **"Live App"** and enjoy!

    ![waiting for deploy](https://user-images.githubusercontent.com/66209958/202896693-06195fff-4c61-4572-a960-48f032fdb82b.png)
    ![success](https://user-images.githubusercontent.com/66209958/202896699-83f8ad49-e741-4114-9b83-0fb608e68baf.png)

</details>


<details>
<summary>Ubuntu Droplet</summary>
<br>

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

3. Follow the steps as shown in [README](https://github.com/aahnik/tgcf/#install-and-run) to install and run tgcf.
4. Closing the console stops the running `tgcf-web` process. You can use a detached [screen](https://www.gnu.org/software/screen/) session to keep tgcf running in the background.

    ```shell
    # make sure you are inside your my-tgcf directory
    screen -S tgcfSession
    source .venv/bin/activate
    tgcf-web
    ```

Exit the screen session by <kbd>Ctrl</kbd> + <kbd>a</kbd> then press <kbd>d</kbd>.
Now you can safely close the console to VPS.
</details>

