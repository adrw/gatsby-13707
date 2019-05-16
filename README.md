# gatsby-13707
Example repo for https://github.com/gatsbyjs/gatsby/issues/13707

[![CircleCI](https://circleci.com/gh/adrw/gatsby-13707.svg?style=svg)](https://circleci.com/gh/adrw/gatsby-13707)

# Suspected Problems
- Rush relies on using symlinks to allow consuming local versions of packages that exist in the monorepo
- Rush also relies on a version set in the consuming package (non `*`) so that it can know whether to link or pull an older version from NPM
- Gatsby seems to by idiom rely on the theme package having `"*"` or is unable to follow the symlinks to the local versions of theme packages

# Local Install Instructions
- `npm install -g @microsoft/rush`
- `nvm use 10.15` (Rush requires Node version `>=8.9.4 < 11.0.0`)
- `rush install`
- `rush build`