[简体中文](https://github.com/gugugagaOJ/OnlineJudgeDeploy/blob/master/README.md) | English


# Environment Setup

### Linux Environment

1. **Install Docker and Docker Compose**

   This project has packaged all dependencies into Docker images. You just need to ensure that Docker and Docker Compose are installed on your system.

   * **Install Docker:**

     * Users in China can use the following script to install Docker with one command:

       ```bash
       sudo curl -sSL https://get.daocloud.io/docker | sh
       ```

     * Users outside of China can use the following script to install Docker with one command:

       ```bash
       sudo curl -sSL get.docker.com | sh
       ```

   * **Install Docker Compose:**

     ```bash
     sudo apt-get update && sudo apt-get install -y docker-compose
     ```

   For detailed installation steps, you can refer to the official documentation: [Docker Installation Docs](https://docs.docker.com/install/)

2. **Install Git and Necessary Tools (Optional)**

   If Git and other common tools are not installed on your system, you can install them with the following command:

   ```bash
   sudo apt-get update && sudo apt-get install -y git curl vim
   ```

   These tools are not mandatory, but they will be useful if you need to perform any custom configurations or debugging.

### Windows Environment

Installation on Windows is for testing purposes only. It is not recommended for production environments. If necessary, please use a virtual machine with Linux and install the OJ (Online Judge) on that.

The following guide is applicable only to **Win10 x64** using `PowerShell`.

1. **Install Docker for Windows**
2. **Right-click the Docker icon in the system tray and select "Settings"**
3. **Go to the "Shared Drives" menu**, and select the drive where you want to install the OJ (e.g., select the D drive). Click `Apply`.
4. **Enter your Windows username and password** to enable file sharing.
5. **Install Python**, `pip`, `git`, and `docker-compose`. The installation methods can be found with a quick search.

## Installation

1. Choose a location with sufficient disk space, and run the following command:

   ```bash
   git clone https://github.com/gugugagaOJ/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy
   ```

2. Start the service:

   ```bash
   docker-compose up -d
   ```

Depending on your internet speed, the setup process will take about 5 to 30 minutes and will be fully automated without requiring manual intervention.

Once the command execution is complete, run `docker ps -a`. When all containers show a status other than `unhealthy` or `Exited (x) xxx`, it means the OJ has been successfully started.

## Enjoy!

You can access the system via the browser at the server's HTTP port 80 or HTTPS port 443. The backend management path is `/admin`. The super admin username created automatically during the installation is `root` with the password `rootroot`. **Please make sure to change the password promptly**.

Don’t forget to check out the documentation at [http://opensource.qduoj.com/](http://opensource.qduoj.com/).

## Customization

Version 2.0 has moved many commonly used settings to the backend management interface. You can directly log in to the management panel to configure the system without modifying the code.

If you need to modify the system or do secondary development, refer to the **README** for each module. After modification, you will need to rebuild the Docker image and modify the `docker-compose.yml`.

## Encounter any issues?

Please refer to: [http://opensource.qduoj.com/](http://opensource.qduoj.com/#/onlinejudge/faq). If you have other issues, join the discussion group or submit an issue.


