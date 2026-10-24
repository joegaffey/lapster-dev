# Lapster Dev

Development preview of [Lapster](https://github.com/joegaffey/lapster), built from a
selected branch and served at <https://joegaffey.com/lapster-dev/>.

The stable site at <https://joegaffey.com/lapster/> is deployed separately and is not
affected by this repository.

## Deploy

The Pages workflow checks out a branch from `joegaffey/lapster`, builds the browser
viewers, and deploys the resulting `dist/` directory.

```sh
gh workflow run pages.yml -R joegaffey/lapster-dev \
  -f ref=feature/directional-shadows
```

The `ref` input accepts any branch or tag in `joegaffey/lapster`.

The build sets `LAPSTER_BUILD_CHANNEL=dev`, which defaults the graphics settings to
Baked environment shadows and Silhouette car shadows and isolates dev settings from the
stable site.
