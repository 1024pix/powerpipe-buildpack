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

## Config files

You can copy put your config files for mods anywhere as *.ppc.erb* and they will be copied to the powerpipe config directory after a pass with *erb*.

Example `datadog.ppc.erb`:

```
connection "datadog" {
  plugin = "datadog"
  api_key = "<%= ENV['DATADOG_API_KEY'] %>"
  app_key = "<%= ENV['DATADOG_APP_KEY'] %>"
  api_url = "https://api.datadoghq.com/"
}
```

[powerpipe]: https://powerpipe.io/
[scalingo]: https://scalingo.com/
