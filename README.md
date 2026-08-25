# ray-index — the raylang package index

One file per package (`<name>.toml`), written by `ray registry publish`: each version maps to
its git URL + tag and the sha256 of the published content (verified on every download).

Consume it from a project's `ray.toml`:

```toml
[registry]
index = "git+https://github.com/ray-language/ray-index@main"

[dependencies]
greeting = "1.0.0"
```

Then `ray fetch` (or just `ray run`). `ray add <name>` picks the latest non-yanked version.
