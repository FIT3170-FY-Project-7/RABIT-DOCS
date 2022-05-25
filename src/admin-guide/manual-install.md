# Manual installation

## Requirements

- [Node.js](https://nodejs.org)

## Installation

1. Clone the repository. We use git submodules so make sure you also cloned all submodules. Then `cd` to 
frontend directory.
```
$ https://github.com/FIT3170-FY-Project-7/RABIT-COMMON
$ cd RABIT-FRONTEND
```

2. Install dependencies
```
$ npm install --save-dev
```

3. Build the frontend. Output files will be placed in `dist`.
```
$ npm run build
```

4. Serve the files in `dist` using your preferred web server, such as [Nginx](nginx.md).

## Update 

Run `git pull --recurse-submodules` then follow the installation instructions again.