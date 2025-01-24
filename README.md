# Rawon

> A simple powerful Discord music bot built to fulfill your production desires. Easy to use, with no coding required.

## Features
- Interaction support.
- Configurable, and easy to use.
- Basic music and moderation commands.
- A production-ready project, set up the bot without coding.

## General Setup
1. Download and install [Node.js](https://nodejs.org) version `16.6.0` or higher
2. Open the `.env_example` file and rename it to `.env`
3. Install required and optional dependencies. You still can use `npm` too.
```sh
$ pnpm install
```
4. Compile the file
```sh
$ pnpm run build
```
5. If you want to save your disk spaces, let's prune the dev dependencies
```sh
$ pnpm prune --production
```
6. Finally, you can start the bot
```sh
$ pnpm start
```


### Docker
You can use our official Docker image:
```bash
$ docker run -v ./scripts:/app/scripts --env-file ./.env -d ghcr.io/stegripe/rawon:latest 
```

...or with docker-compose:
```yml
services:
  rawon:
    image: ghcr.io/stegripe/rawon:latest
    restart: unless-stopped
    env_file: .env
    volumes:
      - "./scripts:/app/scripts"
```

Don't forget to create `.env` file and fill environment values from `.env_example` file

NOTE: You **must** attach `/app/scripts` volume if you use `yt-dlp` stream strategy.

### Glitch
You can use Glitch too for this project, featured with its code editor.

1. Star and fork this project
2. Go to [glitch.com](https://glitch.com) and make an account
3. Click **New Project** then **Import from GitHub**, specify the pop-up field with `https://github.com/<your-name>/rawon` (without `<>`)
4. Please wait for a while, this process takes some minutes
5. Find the `.env` file and delete it, then find `.env_example` file and rename it to `.env`
6. After specifying `.env`, open **Tools** > **Terminal**
7. Type `refresh`, and track the process from **Logs**



**IMPORTANT:** Read [Disclaimers](./DISCLAIMERS.md) before deploying to Railway.


 
## Disclaimers
Disclaimers are listed on the [DISCLAIMERS.md](./DISCLAIMERS.md) file.


