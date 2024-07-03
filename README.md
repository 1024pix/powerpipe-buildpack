# Buildpack: Powerpipe

Run [Powerpipe][] using buildpacks.

Use with [Scalingo][]: `scalingo env-set BUILDPACK_URL=https://github.com/1024pix/powerpipe-buildpack`

## Configuration

- `POWERPIPE_VERSION`: the version of powerpipe to install, latest by default (eg: `POWERPIPE_VERSION=v0.4.0`)

## Procfile

**With dashboard**:

```
web: ./bin/powerpipe server --port $PORT
```

[powerpipe]: https://powerpipe.io/
[scalingo]: https://scalingo.com/
