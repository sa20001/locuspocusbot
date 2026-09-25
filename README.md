# LocusPocusBot 3.0

> [!NOTE]
> **LocusPocusBot 3.0** is a community-maintained continuation of the original LocusPocusBot.
>
> The original [**LocusPocusBot**](https://github.com/matteocontrini/locuspocusbot) was discontinued in December 2025. This version has been independently redeployed.

## Requirements

MongoDB is required for the bot to work. Data about users and groups will be stored in the database.

## Configuration

Configuration of the application is done through the `appSettings.json` file read from the current working directory at startup.

## Running in production

For running in production refer to `docker-compose.yaml`.

## Running for development

Choose one of the following methods:

### Visual Studio

Requirements:

- .NET 6.0 SDK is installed
- MongoDB is running on the host and port specified in the `appSettings.json` file
- The `LocusPocusBot/bin/Debug/net6.0` directory contains the `appSettings.json` file

Run with the nice green button.

### dotnet CLI

Requirements:

- .NET 6.0 SDK is installed
- MongoDB is running on the host and port specified in the `appSettings.json` file
- The `LocusPocusBot` directory contains the `appSettings.json` file

Run with the dotnet CLI by executing:

```sh
cd LocusPocusBot
dotnet run
```

### Docker Compose

Refer to `docker-compose_dev.yaml` and run this command in the repository directory:

```sh
docker-compose -f docker-compose_dev.yaml up --build
```