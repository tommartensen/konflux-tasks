# StackRox Konflux tasks

This repo provides shared Tekton tasks to build ACS/StackRox product in Konflux.

Tasks themselves are in `tasks/` directory.

`.tekton/` directory has the pipeline to package and push tasks as Tekton bundle OCI image for use in pipelines.

## Development

For as long as there are no automated tests ([ROX-27386](https://issues.redhat.com/browse/ROX-27386) is to add them), you should open PRs in consuming repos when changing tasks in order to validate your changes.

Make sure you update bundle references in your consuming pipelines to the value returned in `BUNDLE_REF` the build pipeline here.

Consuming repos are:
* <https://github.com/stackrox/stackrox>
* <https://github.com/stackrox/collector>
* <https://github.com/stackrox/scanner>
