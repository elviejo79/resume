# resume.yaml
Write your resume in yaml and display in a nice formated page.

https://jsonresume.org/ is a great idea. 

Write your resume in a structured format (resume.json) 
store it in github gist like this (https://gist.github.com/thomasdavis/c9dcfa1b37dec07fb2ee7f36d7278105)
And then it can be pretty printer using your username (https://registry.jsonresume.org/thomasdavis )

However I prefer to write yaml rather than json.
So this repository has a resume.yaml file with a github action gets transformed to the necesary gist.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/elviejo79/)

## Basic functionality.
The easy way to host your resume is by making a `resume.json` on gist.github.com. 

For example mine can be found at https://gist.github.com/thomasdavis/c9dcfa1b37dec07fb2ee7f36d7278105 which then automatically gets hosted at https://registry.jsonresume.org/thomasdavis 

You can just edit your Gist using the online GUI and it should update within less than a minute. 

## But

If you would like to have your `resume.yaml` in a repository aka like this. 

You can set up a Github Action that automatically updates your gist `resume.yaml` to match what is in your repo everytime you push. 

If you checkout the `.github/workflows/gist.yml` file you should be able to figure it out with relative ease.  

## The basic steps are 

- [ ] Create a gist called `resume.json`
- [ ] Create or fork this repo and commit your updated `resume.json` 
- [ ] Create a Personal Github token that has just the `gist` scope 
- [ ] Go to your repository settings, then to the secrets page, and add a new secret called `TOKEN` with the value being from the token you created in 3) 
- [ ] Now simply push to your repo, and your `resume.yaml` from the repo, will publish and override your gist `resume.json` and thus updating the registry to match

Enjoy!
