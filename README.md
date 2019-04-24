# ghpages

Deploy angular application on GitHub Pages with custom domain over https

## requirements

+ nodejs

## steps

+ (optional) install `angular-cli`/`angular-cli-ghpages` and create a new project

```
npm install -g @angular/cli angular-cli-ghpages
ng new ghpages --directory .
ng serve --open
```

+ add new build script in `package.json`

```
# without custom domain
"ghpages": "ng build --prod --base-href https://loivis.github.io/github-pages-in-angular/ && npx ngh --dir dist/ghpages"
# with custom domain
"ghpages": "ng build --prod --base-href https://github-pages-in-angular.kinase.wang/ && npx ngh --cname github-pages-in-angular.kinase.wang --dir dist/ghpages"
```

+ build and publish application

```
npm run ghpages
```

+ (optional) add custom domain `CNAME` record in DNS provider

```
github-pages-in-angular.kinase.wang -> loivis.github.io
```

+ (optional) wait for certificate to be available and enable https in project settings

+ woohoo~~~ I'm online

[without custom domain over https, click me!](https://loivis.github.io/github-pages-in-angular/)

[with custom domain over https, click me!](https://github-pages-in-angular.kinase.wang/)

:confused: in case of 404 which is just a matter of delay, try

[index.html without custom domain](https://loivis.github.io/github-pages-in-angular/index.html)

[index.html with custom domain](https://github-pages-in-angular.kinase.wang/index.html)
