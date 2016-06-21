# o2r Web API

_Please note: this document is still a very rough draft and will change a lot._

Project description: http://o2r.info

## Build

This specification is written in [Markdown](https://daringfireball.net/projects/markdown/). You can use `mkdocs` to render it locally, or view the latest master-branch on <http://o2r.info/o2r-web-api/>.

### Automated Builds

[![Build Status](https://travis-ci.org/o2r-project/o2r-web-api.svg?branch=master)](https://travis-ci.org/o2r-project/o2r-web-api)

The current master branch is automatically built on Travis CI and deployed to the GitHub Page at <http://o2r.info/o2r-web-api/>. Our combination of the `.travis.yml` and `.deploy.sh` will run the `mkdocs` command on every direct commit or merge on the master branch and deploy the rendered HTML documents to the `gh-pages` branch in this repository.

Travis authenticates its push to the `gh-pages` branch using a [personal access token](https://github.com/settings/tokens) of the user [@o2r-user](https://github.com/o2r-user). The access token is encrypted in the `.travis.yml` [using Travis CLI](https://docs.travis-ci.com/user/encryption-keys/) _for the repository o2r-project/o2r-web-api_:

```
travis encrypt GH_TOKEN=<token here>
```

The variable `GH_TOKEN` is used in the deploy script. The token generated on the GitHub website should not be stored anywhere, simply generate a new one if needed.

This has some security risks, as described [here](https://gist.github.com/domenic/ec8b0fc8ab45f39403dd#sign-up-for-travis-and-add-your-project). To mitigate these risks, we have disabled the option "Build pull requests" is on the [Travis configuration page for this repo](https://travis-ci.org/o2r-project/o2r-web-api/settings), so that malicious changes to the Travis configuration file will be noticed.


## License

The o2r Web API specification is licensed under Creative Commons CC-BY-4.0 License, see file `LICENSE`.

Copyright (C) 2016 - o2r project.
