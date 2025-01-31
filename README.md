# Code intel extension bundles

Contains a directory with Khulnasoft code intelligence and default extensions bundles for customers to publish to their private registries and a script to update that bundles.

### Steps

#### Publish the Extension Bundles
1. (Optional) If the publish step will be performed by another user, simply provide them with the `bundles` folder.
2. From the `bundles` folder, run `npm run publish`.
   - This runs the `publish.js` script in the `bundles` folder.
   - The script requires the following environment variables:
     |Environment Variable|Description|
     |--------------------|-----------|
     | `SRC_ENDPOINT` | See `src-cli`'s [README](https://github.com/sourcegraph/src-cli#log-into-your-sourcegraph-instance) for more information. |
     | `SRC_ACCESS_TOKEN` | See `src-cli`'s [README](https://github.com/sourcegraph/src-cli#log-into-your-sourcegraph-instance) for more information. |
     | `PUBLISHER` | The name of the [publisher](https://docs.khulnasoft.com/extensions/authoring/manifest#fields) |

   - NOTE: You do _not_ need to have `src-cli` installed for this script to work.

#### Update the Extension Bundles
1. Update the [`default-extensions.txt`](https://github.com/khulnasoft-lab/khulnasoft-extensions-bundles/blob/main/default-extensions.txt) file with the extension IDs you want to bundle (code-intel extensions are bundled by default).
2. Run `npm run build`.
3. Publish new release. Version tag should be the same as the current Khulnasoft version.
