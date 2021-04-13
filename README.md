## Introduction
This is a Dockerfile to build a debian based container image running nginx and php-fpm 7.3.x / 7.2.x / 7.1.x / 7.0.x & Composer.

### Versioning
| Docker Tag | GitHub Release | Nginx Version | PHP Version | Debian Version |
|-----|-------|-----|--------|--------|
| latest | master Branch |1.17.2 | 7.3.8 | buster |


## How to use this repository
The build is automatically triggered by a git push to your feature/[branch]

## First clone the repository to your workstation
```
$ git clone https://github.com/adilshehzad786/Website-deployment-Automation-with-Continuous-Integration-Using-AWS-Jenkins-GitHub.git
```

Create a feature branch. # Always start with feature/[name of your branch]
```
git branch -b feature/add-css-style-to-about-us-page
```


Update the application code in
```
./html/
```

Then add/commit/push to github

```
git status # to see your changes
```

```
git add --all # If you are satisfied with your changes and willing to push everything. Otherwise, select only the files to add
```

```
git commit -m "Put some message about this push here"
```

## Push your changes to gitlab, and merge to dev branch
```
git push --set-upstream origin feature/[Your branch name]
```

## pulling the image
```
docker pull eu.gcr.io/$environment/frontend-propitix:$tag-version
```

## Running (You can do this step without the pulling the above as it will put down if not found locally)
To run the container:
```
$ docker run -d eu.gcr.io/$environment/frontend-propitix:$tag-version
```

Default web root:
```
/usr/share/nginx/html
```

## 
Full Blog is available here : 