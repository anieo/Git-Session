# Git-Session 

A Free Open Source DVCS ”distributed version control system ” 

# How it Works!

- #### Snapshots, Not Differences
  - Compares SHA1 sum of modified files.
  - Saves the new file as a Whole "easier to retrive lost data"
  - Each Snapshot contains references to the files "to save space uses ref. only"
- #### Stores new versions of files only
- #### Each snapshot contains each file
- #### Everything is local “distributed”
    - Each Computer has all the history of the project
    - Makes it faster and easeir to contribute 
    - Safer beacuase the data are not onlt on one repo
- #### Git has Integrity
    - Everything in Git is CHECKSUMMED "fast ,reliable"
    - Uses SHA-1 hash "a 40 hexadecimal char string"
    - Easy to recognize corrupted files.
- #### Git Generally Only Adds Data "Everything is almost reversible"



## Files’ Three States
- Modified
- Staged
- Committed

## Installtion
```sh
$ sudo apt update
$ sudo apt intsall git
```

## First Time Configurations 
```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --global merge.tool meld 
```

## Git Help
git has a really good command manual for each command
```sh
$ git help <command>
$ man git <command>
$ git <command> -h #summarized
```
## Important Terms
- Repository
- Index “Staging area”
- working tree “Project tree”
- Commit
- Branch
- Tag
- Master
- Head
# Git Basics
- #### Git Repository
```sh
$ git init # Intialize a Embty/new repository
$ git clone <URL># to Clone/Copy exsiting repository
```
 `<URL>`: can be git, shh, http, https, file , etc 
- ## Recording Changes to the Repository [![N|Solid](./pasted%20image%200.png)
    - #### Checking status of your files
        ```sh
        $ git status`
        $ git status -s # Summarized
        ```
        - `??`    “ untraked ”
        - A     “ staged ”
        - M     “ Modified staged “ 
        - `M`    “ Modified untracked “
        Example: 
        ```sh
        $ git status
        $ echo 'I' > README #creates a new file
        $ git status
        ```
    - #### Staging Modified Files
        Stage your files after adding not before
        ``` sh
        $ git add <files|WildCards> 
        ```
        Example:
        ```sh
        $ git add README
        $ git status
        $ echo “USE” >> README
        $ git status
        $ git add README
        $ git status
        ```
    - #### Ignoring Files
        A file listing patterns to match them with files in your repositories.
        File name “.gitignore”
        - .gitignore [`common templates`](https://github.com/github/gitignore)
        - See `man gitignore` for more information
    - #### Viewing staged and unstaged
        ``` sh
        $ git status
        $ git diff
        $ git diff --staged
        ```

    
- ## Commit History
- ## Undoing Things
- ## Working with Remotes
- ## Tags and Aliases
> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Tech

Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [Breakdance](http://breakdance.io) - HTML to Markdown converter
* [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| Github | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MORE Tests
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
