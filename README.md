<div align ="center">

<img src="projectInfo/icon.png" width="180">

# MCServerTemplate

<span style="font-size:18px;">An easily deployable Minecraft server template.</span>

[![CodeFactor](https://www.codefactor.io/repository/github/etcherfx/mcservertemplate/badge/main?style=for-the-badge)](https://www.codefactor.io/repository/github/etcherfx/mcservertemplate/overview/main)
[![License](https://img.shields.io/github/license/etcherfx/MCServerTemplate?style=for-the-badge)](https://github.com/etcherfx/MCServerTemplate/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/etcherfx/MCServerTemplate?style=for-the-badge)](https://github.com/etcherfx/MCServerTemplate/issues) <br>
[![GitHub Release](https://img.shields.io/github/release/etcherfx/MCServerTemplate?include_prereleases&style=for-the-badge)](https://github.com/etcherfx/MCServerTemplate/releases/latest)

</div>

## Links

- [Releases](https://github.com/etcherfx/MCServerTemplate/releases)

## Projects Used

- [Simerlol's Minecraft Server Template](https://replit.com/@SimerLol/Minecraft-Server-Template)

## Deployment

### Method 1 - Deploy from Github:

<a href="https://replit.com/github/etcherfx/MCServerTemplate" target="_blank"><img src="https://binbashbanana.github.io/deploy-buttons/buttons/remade/replit.svg" alt="Run on Replit"></a>

- Open the `Run on replit` button in a new tab and press `Import from Github`

  <img src="projectInfo/importGithub.png" width="550">

### Method 2 - Manual Cloning:

- Create a new `Bash` repl

   <img src="projectInfo/createRepl.png" width="450">

- Type the following command into the shell:
  ```
  git clone https://github.com/etcherfx/MCServerTemplate.git && shopt -s dotglob && mv MCServerTemplate/* MCServerTemplate/../ && rm -rf MCServerTemplate main.sh
  ```

## Setting Java Versions

- In the files section on replit, click the three dots and click `Show hidden files`

  <img src="projectInfo/replitHiddenFiles.png" width="350">

- Navigate to `replit.nix` and follow these intructions:
  - For Minecraft 1.16.x and below, do not change anything.
  - For Minecraft 1.17.x and above, make sure to change `pkgs.openjdk8-bootstrap` to `pkgs.openjdk17-bootstrap`

## Creating Enviornment Variables

- Click on the `Secrets` button in the tools section on the far left side of your screen

  <img src="projectInfo/replitTools.png" width="350">

- Create a new secret called `ngrok_region` and input one of the regional codes from the list below as the value:

  > _Choose the closest region for better network connectivity._

  | Region                    | Code |
  | ------------------------- | ---- |
  | United States (Ohio)      | `us` |
  | Europe (Frankfurt)        | `eu` |
  | Asia/Pacific (Singapore)  | `ap` |
  | Australia (Sydney)        | `au` |
  | South America (Sao Paulo) | `sa` |
  | Japan (Tokyo)             | `jp` |
  | India (Mumbai)            | `in` |

  <img src="projectInfo/replitSecrets.png" width="450">

- Do the same for the variables in the list below:

  | Key           | Value                                                                                                |
  | ------------- | ---------------------------------------------------------------------------------------------------- |
  | `ngrok_token` | Your [authtoken](https://dashboard.ngrok.com/get-started/your-authtoken) for ngrok.                  |
  | `SERVER`      | The server software in all lowercase. e.g `purpur`                                                   |
  | `VERSION`     | Version of Minecraft your server is running on. e.g `1.19.4`                                         |
  | `BUILD`       | The build number of your server software. _Only use this if you have `paper` as the server software_ |

  > _If you don't have a ngrok authtoken, you can [visit here](https://dashboard.ngrok.com/get-started/your-authtoken) and make an account to get your token._

  <img src="projectInfo/authToken.png" width="350">

- List of server software supported:

  - [Purpur](https://purpurmc.org/)
  - [Paper](https://papermc.io/)
  - [Magma](https://magmafoundation.org/)

- Here are some recommended build numbers for `paper`:

  | Minecraft Version | Build # |
  | ----------------- | ------- |
  | `1.20.1`          | `124`   |
  | `1.19.4`          | `550`   |
  | `1.18.2`          | `388`   |
  | `1.17.1`          | `411`   |
  | `1.16.5`          | `794`   |
  | `1.15.2`          | `393`   |
  | `1.14.4`          | `245`   |
  | `1.13.2`          | `657`   |
  | `1.12.2`          | `1620`  |
  | `1.11.2`          | `1106`  |
  | `1.10.2`          | `918`   |
  | `1.9.4`           | `775`   |
  | `1.8.8`           | `445`   |

  > _To get a list of all build numbers for paper, visit [here](https://papermc.io/downloads/all)_

## Running the Server

- Run the repl and follow the instructions on the console
- Once the console displays `Done! For help, type "help"`, navigate to `status.log` and copy the IP address on `line 7` and enter it inside of Minecraft. The IP should be something like `tcp://9.tcp.eu.ngrok.io:46797` and you want to copy the whole address **EXCEPT** the `tcp://` part.

## Server Optimization

- Boost your repl
- Follow [this](https://github.com/YouHaveTrouble/minecraft-optimization) server optimization guide
