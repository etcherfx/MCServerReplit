<h1 align="center">
  <img src="projectInfo/banner.png" alt="MCServerReplit Banner" width="850">
</h1>
  
<div align="center">

[![CodeFactor](https://www.codefactor.io/repository/github/etcherfx/mcserverreplit/badge/main?style=for-the-badge)](https://www.codefactor.io/repository/github/etcherfx/mcserverreplit/overview/main)
[![License](https://img.shields.io/github/license/etcherfx/MCServerReplit?style=for-the-badge)](https://github.com/etcherfx/MCServerReplit/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/etcherfx/MCServerReplit?style=for-the-badge)](https://github.com/etcherfx/MCServerReplit/issues)
[![GitHub Release](https://img.shields.io/github/release/etcherfx/MCServerReplit?include_prereleases&style=for-the-badge)](https://github.com/etcherfx/MCServerReplit/releases/latest)

**An easily deployable Minecraft server template for Replit.**

A fork of SimerLol's [Minecraft Server Template](https://replit.com/@SimerLol/Minecraft-Server-Template)

</div>

> [!WARNING]
> This project is now archived. Replit has become increasingly unusable due to excessive AI integration and paywalls, making it no longer a suitable platform for this project.

## 📖 Table of Contents

- [📖 Table of Contents](#-table-of-contents)
- [🔗 Links](#-links)
- [🚀 Deployment](#-deployment)
- [⚙️ Setting Java Versions](#️-setting-java-versions)
- [🔐 Creating Environment Variables](#-creating-environment-variables)
  - [Supported Server Software](#supported-server-software)
  - [Recommended Paper Build Numbers](#recommended-paper-build-numbers)
- [🏃 Running the Server](#-running-the-server)
- [⚡ Server Optimization](#-server-optimization)

## 🔗 Links

- [Releases](https://github.com/etcherfx/MCServerReplit/releases)

## 🚀 Deployment

Navigate to the [import page](https://replit.com/import/github) on Replit and paste the repository URL:

```
https://github.com/etcherfx/MCServerReplit
```

Click on the `Import from GitHub` button

<img src="projectInfo/importGithub.webp" alt="Import from GitHub button" width="400">

## ⚙️ Setting Java Versions

1. In the files section on replit, click the three dots and hit `Show hidden files`

   <img src="projectInfo/replitHiddenFiles.png" alt="Show hidden files option" width="350">

   > **Note:** Sometimes, there might only be a `Hide hidden files` option. In that case, you already have hidden files shown.

2. Navigate to the `replit.nix` file and click on it to open it

   <img src="projectInfo/replitNix.png" alt="replit.nix file location" width="250">

3. Choose the Java version you want to use from below and replace the default Java version with the one you want to use:

   > **Note:** The default Java version is `pkgs.jdk21_headless`

   | Minecraft Version | Java Version               |
   | ----------------- | -------------------------- |
   | `1.21+`           | `pkgs.jdk21_headless`      |
   | `1.17 - 1.20`     | `pkgs.openjdk17-bootstrap` |
   | `1.16-`           | `pkgs.openjdk8-bootstrap`  |

## 🔐 Creating Environment Variables

1. Click on the `Secrets` button in the tools section on the far left side of your screen

   <img src="projectInfo/tools.webp" alt="Tools section" width="400">

2. Click on the `New secret` button

   <img src="projectInfo/replitSecrets.png" alt="New secret button" width="550">

3. Create a new secret with the key named `ngrok_token` and the value as your [authtoken](https://dashboard.ngrok.com/get-started/your-authtoken)

   > **Note:** You need to create an ngrok account to get an authtoken

4. Do the same for the variables in the list below:

   | Key       | Value                                                                                                |
   | --------- | ---------------------------------------------------------------------------------------------------- |
   | `SERVER`  | The server software in all lowercase. e.g `purpur`                                                   |
   | `VERSION` | Version of Minecraft your server is running on. e.g `1.19.4`                                         |
   | `BUILD`   | The build number of your server software. _Only use this if you have `paper` as the server software_ |

### Supported Server Software

- [Purpur](https://purpurmc.org/) (1.16.1 and above)
- [Paper](https://papermc.io/) (1.8.8 and above)

### Recommended Paper Build Numbers

| Minecraft Version | Build # |
| ----------------- | ------- |
| `1.21.4`          | `232`   |
| `1.20.6`          | `151`   |
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

> **Tip:** To get a list of all build numbers for paper, visit [PaperMC Downloads](https://papermc.io/downloads/all)

## 🏃 Running the Server

1. Run the repl and follow the instructions on the console
2. Once the console displays `Done! For help, type "help"`, scroll up to the top of the console output and copy the server address
   - It should look something like `0.tcp.ngrok.io:12345`
3. Paste the server address in your Minecraft client and join the server

## ⚡ Server Optimization

- Follow [this server optimization guide](https://github.com/YouHaveTrouble/minecraft-optimization) for optimal performance
