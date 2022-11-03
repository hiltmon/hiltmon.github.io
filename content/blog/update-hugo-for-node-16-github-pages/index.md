---
title: "Update Hugo for Node 16 Github Pages"
date: 2022-11-03T12:23:01-04:00
author: Hilton Lipschitz
tags: [ Hugo, GitHub ]
---

Recently, GitHub updated actions from Node 12 to Node 16 (See [GitHub Actions: All Actions will begin running on Node16 instead of Node12](https://github.blog/changelog/2022-09-22-github-actions-all-actions-will-begin-running-on-node16-instead-of-node12/)). As a result, Hugo deploys will fail. All I saw was that I committed the updated site, and the deploy did not happen.

To make it work again, you need to update your `gh-pages.yml` in the hidden `.github/workflows` folder to reflect the new Ubuntu and `checkout` versions:

<!-- more -->

```
...
jobs:
  deploy:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v3
        with:
          submodules: true  # Fetch Hugo themes (true OR recursive)
...
```

Diff is:

{{< figure src="images/hugo-github-pages-update-2022.png" width=640 height=102 >}}

And deploy works again.
