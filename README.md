# com-lint [bot]

[![npm](https://img.shields.io/npm/v/commitlint-bot.svg)](https://www.npmjs.com/package/commitlint-bot)

[![npm](https://img.shields.io/npm/v/@ammar-ahmed/automation-app-bot.svg)](https://www.npmjs.com/package/@ammar-ahmed/automation-app-bot)



<p align="center">
  <img src="docs/robot.svg" width="256" alt="commitlint logo" />
</p>

> Built with [probot](https://github.com/probot/probot) framework

A GitHub App that runs [commitlint](https://github.com/marionebl/commitlint) against all commits of new or edited pull requests
and sets an appropriate status check.

## Usage

1.  Browse to [GitHub Apps - commitlint][apps]
2.  Accept the permissions 
3.  Allow access to repositories

On the next pull request, a status check from `commitlint` will appear:

![status-check-screenshot][]

Problem details will be reported as a comment like this:

![status-comment-screenshot][]

For best results, enable branch protection (in the repository's settings) and require the `commitlint` status check to pass before merging:

![branch-protection-screenshot][]

[apps]: https://github.com/apps/com-lint
[status-check-screenshot]: docs/status.png
[status-comment-screenshot]: docs/comment.png
[branch-protection-screenshot]: docs/setting.png

## What is missing?

We don't currently support custom configuration (i.e. `.commitlint.yml` or `.commitlint.json`), but [we will](https://github.com/Ammar-Knowledge/com-lint/issues)

## Development

1.  Setup the repo:

```shell
git clone https://github.com/Ammar-Knowledge/com-lint.git
cd com-lint
npm install
```

2.  Create your own [GitHub app][]
3.  Store the private key as `private-key.pem` somewhere safe, and point to its location in `.env`
4.  Start the app with `APP_ID=1234 npm start` where `1234` is your GitHub app's ID
5.  Update your GitHub app's Webhook URL to your localtunnel.me URL

[github app]: https://probot.github.io/docs/development/#configure-a-github-app

## Deployment

See [docs/deploy.md](./docs/deploy.md) for more info.

## Credits

Robot designed by [Freepik](https://www.freepik.com/free-vector/fun-pack-of-robots-avatars_1258314.htm).

Inspired by the awesome work of Tom Vincent in their [validate-commit-msg-bot](https://github.com/tlvince/validate-commit-msg-bot) package.


## License

MIT © [Ammar-Ahmed-Butt](https://github.com/ammar-ahmed-butt)
