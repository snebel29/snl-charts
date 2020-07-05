# SNL Charts Repo

Hosting for my own helm charts

### Why?

https://snebel29.github.io/2019/08/21/use-github-pages-to-host-your-helm-charts/

### How It Works

I set up GitHub Pages to point to the `docs` folder. From there, I can
create and publish charts like this:

```console
$ helm package kwatchman/
$ mv kwatchman-0.1.0.tgz docs/
$ helm repo index docs --url https://snebel29.github.io/snl-charts
$ git add --all
$ git commit -m "Adding kwatchman"
$ git push origin master
```

### Adding this repository on helm
From there, You can add it as helm repository and install any of the available charts.

```console
$ helm repo add snl-charts https://snebel29.github.io/snl-charts
```
