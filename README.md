# Mintlify Starter Kit

Use the starter kit to get your docs deployed and ready to customize.

Click the green **Use this template** button at the top of this repo to copy the Mintlify starter kit. The starter kit contains examples with

- Guide pages
- Navigation
- Customizations
- API reference pages
- Use of popular components

**[Follow the full quickstart guide](https://starter.mintlify.com/quickstart)**

## AI-assisted writing

Set up your AI coding tool to work with Mintlify:

```bash
npx skills add https://mintlify.com/docs
```

This command installs Mintlify's documentation skill for your configured AI tools like Claude Code, Cursor, Windsurf, and others. The skill includes component reference, writing standards, and workflow guidance.

See the [AI tools guides](/ai-tools) for tool-specific setup.

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

If install scripts were blocked (common with recent npm), also allow `keytar` so login works:

```
npm i -g mint --allow-scripts=keytar,sharp,@scarf/scarf
```

Authenticate once (required for **local search** and the assistant):

```
mint login
```

Then from the docs root (`docs.json`):

```
mint dev
```

View your local preview at `http://localhost:3000`.

### Search & environment variables

- Local preview search needs `mint login` — there is **no** `docs.json` env var for it.
- Deployed Mintlify sites get search from the Mintlify project (GitHub app / dashboard), not from `.env`.
- Mintlify only uses env vars in **headless** setups (`PUBLIC_MINTLIFY_SUBDOMAIN`, `PUBLIC_MINTLIFY_ASSISTANT_KEY`). This repo is a standard Mintlify site, so navbar/support links are plain URLs in `docs.json`.

## Publishing changes

Install our GitHub app from your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app) to propagate changes from your repo to your deployment. Changes are deployed to production automatically after pushing to the default branch.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)
