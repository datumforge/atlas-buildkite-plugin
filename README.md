[![Build status](https://badge.buildkite.com/13f3af0eff5da18c35e2f5f48831f28b395d0adee4c940c92e.svg?branch=main)](https://buildkite.com/datum/atlas-buildkite-plugin)

# Atlas Buildkite Plugin 

Buildkite plugin that will `lint` and `migrate` [atlas](https://atlasgo.io/cloud/) db schemas

## Example

Add the following to your `pipeline.yml`:

```yml
steps:
  - plugins:
      - datumforge/atlas#v0.0.2:
          dir: file://db/migrations
          project: datum
          dev-url: sqlite://dev?mode=memory
          step: all
```

## Environment Variables

The `ATLAS_CLOUD_TOKEN` is required to be set in the environment before the plugin can run

## Developing

To run the linter:
```shell
task lint
```

To run the tests:

```shell
task test
```

## Contributing

1. Fork the repo
2. Make the changes
3. Run the tests
4. Commit and push your changes
5. Send a pull request
