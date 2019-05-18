# travis-pipeline-buildkite-plugin

Use [travis-pipeline](https://github.com/keithduncan/travis-pipeline) to
automatically translate a Travis CI config into a Buildkite pipeline.

This can be used to create a Buildkite pipeline for a forked repository
that includes a Travis CI config and run the CI jobs on your own Buildkite
agents for improved performance.

## Example

```yml
steps:
  - label: ":pipeline:"
    agents:
      queue: "ecs/agents"
      travis-pipeline: true
    plugins:
      - "keithduncan/travis-pipeline#v0.3":
          queue: "ecs/agents"
          tags:
            - "rust:embedded=true"
```
