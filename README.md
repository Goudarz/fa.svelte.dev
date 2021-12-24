# template-svelte.dev

Template repository to start translating `svelte.dev` site.


## Setup the repository

Clone this repo as template and edit folowing things:

* *package.json*
    - Replace `"name": "template-svelte.dev"` -> `"name": "lang-svelte.dev"` (Ex. `"name": "ru-svelte.dev"`)
    - Edit description

* *patch/strings.json*
    - Edit path to the tutorial folder in your new translation-repository
    - Edit props for the Docs repo edit link also.

## Getting started
Translation process is based on [translation-patcher](https://www.npmjs.com/package/trpatcher) utility. So you can run this command inside your repo dir:
```shell
$ npm run dsa
```
This cause downloading, installing dependencing and replacing files by translated ones from the `patch` folder. 

Then you can run site in development mode:

```shell
$ npm run dev
```

Open your browser on http://localhost:3000 to see the looking of the translated site.

There are some original files in the `patch` directory. Translate them(check for actuality!) and then add more original files and translate them too. 

*TIP:* you can easy copy original files from the `__BUILD` directory. They are actual as soon as you runned `npm run dsa` or `npm run download` comands.

Also there is `strings.json` file in the `patch` folder. Inside you may write many original-translated strings pairs groupped by filenames. `trpatcher` will replace strings in theese files, it is useful in situation when logic of the site components changed during time but text is still here.

When site is running in development mode, every time you change files in `patch` folder they will be merged with original files. So you can see actual translation in the browser(maybe reload nedded).

## Building

If you want to run site in production environment. Run this commands:

```shell
$ npm run build
$ npm run start
```

Translated site will be builded and launched on http://localhost:3000 in production mode.