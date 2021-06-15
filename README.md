# Standard Notes Extensions

[![Netlify Status](https://api.netlify.com/api/v1/badges/25256400-19de-4a55-a026-3d8ced3bf9b7/deploy-status)](https://app.netlify.com/sites/standardnotes-extensions/deploys)

## Features

1. Updated daily (GitHub Actions using ```schedule```)
2. Contains Official and custom extensions

## Suggest new extensions

Open a Pull Request to add new extensions.  
Alternatively, open an Issue to suggest new extensions.    

## Usage

### Option 1: Use default URL

Use ```https://standardnotes-extensions.netlify.app/index.json``` as an *Extended Code* in Standard-Notes.

### Option 2: Fork & Use custom URL (with [Netlify](https://app.netlify.com/))

1. Fork this repo [benjaminjacobreji/standardnotes-extensions](https://github.com/benjaminjacobreji/standardnotes-extensions/fork)
2. Sign-in/ Sign-up into [Netlify](https://app.netlify.com/)
3. Click on [New site from Git](https://app.netlify.com/start) Button.
4. Connect to GitHub and select forked repo  ```your-github-username/standardnotes-extensions```
5. Deploy site and wait for build to finish
6. (Optional) Change Site name at ```Site settings > Change site name``` on Netlify
7. After that you can use ```YOUR_SITE_URL/index.json``` as an ```Extended Code```

### Option 3: Fork & Use custom URL (without [Netlify](https://app.netlify.com/))

It's easy and recommended to host with Netlify. However if you insist not to use it, it is also possible (notice: the following steps work on Linux or WSL):

1. Prepare your environment with `Python 3.7` with `pip`, as well as `Git`;
2. Make sure Python 3.7 can be called directly via `python` from the shell;
3. Make sure Git is installed and can be called directly via `git` from the shell;
4. `pip install -r requirements.txt` to install required Python libraries;
5. Run the build script `URL=my_url python build.py` where `my_url` is the full URL you would later host the resource files on. E.g. if you want to access the plugins via `https://example.com/index.json` then replace `my_url` with `https://example.com/`.
6. Verify that:
    1. the `public` directory is generated;
    2. there should be `public/index.json` containing information of all extensions;
    3. all extensions should exists in `public` as sub-directories;
7. Host the `public` directory like you would do with any static resources, using nginx, caddy, etc.
8. You need to enable CORS headers on your reverse proxy (nginx / caddy / traefik). With nginx these rules will be enough:
    ```nginx
    add_header 'Access-Control-Allow-Origin' '*';
    add_header 'Access-Control-Allow-Headers' 'content-type';
    ```

## Credits

Huge thanks to all these contributors and other authors.

1. [standardnotes](https://github.com/standardnotes)
2. [sn-extensions](https://github.com/sn-extensions/)
3. [JokerQyou/snextensions](https://github.com/JokerQyou/snextensions)
4. [iganeshk/standardnotes-extensions](https://github.com/iganeshk/standardnotes-extensions)
5. [kylejbrk/standard-notes-open-extended](https://github.com/kylejbrk/standard-notes-open-extended)
