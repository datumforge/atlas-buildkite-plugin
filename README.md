# Atlas Buildkite Plugin 

Buildkite plugin that will lint and migrate atlas db schemas. 

## Example

Provide an example of using this plugin, like so:

Add the following to your `pipeline.yml`:

```yml
steps:
  - plugins:
      - datumforge/atlas#v0.0.1:
          dir: file://db/migrations
          project: datum
          dev-url: sqlite://dev?mode=memory
          step: all
```

## Environment Variables

The `ATLAS_CLOUD_TOKEN` is required to be set in the environment before the plugin can run

## Developing

Provide examples on how to modify and test, e.g.:

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