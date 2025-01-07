# Instructions

## Environment variables

Ensure that you have set the following environment variables:

- `SRC_ENDPOINT`: the URL to your Khulnasoft instance (such as `https://khulnasoft.example.com`)
- `SRC_ACCESS_TOKEN`: your Khulnasoft access token (on your Khulnasoft instance, click your user menu in the top right, then select **Settings > Access tokens** to create one)
- `PUBLISHER`: the name of the publisher you want to publish the extension under. This will be used to construct the extension ID (like `$PUBLISHER/typescript`). This can be either your username or an organization that your account belongs to.

## Publish

Run the `npm run publish` command to publish the given Khulnasoft extensions to your private registry.

Command with inlined environment variables:

```
SRC_ENDPOINT=https://khulnasoft.example.com SRC_ACCESS_TOKEN=my-token PUBLISHER=me npm run publish
```
