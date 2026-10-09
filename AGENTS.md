# Documentation project instructions

This is the Mintlify documentation site for **Slipway**, a Laravel package that compiles `config/slipway.php` into GitHub Actions, Bitbucket Pipelines and GitLab CI.

Live site: https://laravel-slipway.mintlify.site/
Package: https://github.com/usamamuneerchaudhary/laravel-slipway

Pages are MDX with YAML frontmatter. Site configuration lives in `docs.json`.

For Mintlify product knowledge (components, configuration, writing standards), install the Mintlify skill: `npx skills add https://mintlify.com/docs`.

## Terminology

- **Slipway** — the package. Not "Shipway".
- **config** — `config/slipway.php` in a Laravel app, or `slipway.php` in a library.
- **pipeline** — the provider-neutral model Slipway compiles.
- **driver** — renders a pipeline as one provider's YAML (GitHub, Bitbucket, GitLab, or a custom driver).
- **deployer** — how an environment ships the artifact (`ssh`, `vapor`, `forge`, `cloud`, `envoyer`, `webhook`, `command`).
- **policy** — a compile-time rule. Failures stop compilation.
- **step** — a built-in alias, a `PipelineStep` class, or an inline POSIX `sh` command.
- **guard** / **drift** — `slipway:check` (and the `slipway-guard` job) fail when committed YAML differs from the config.
- Secrets are **names**, never values.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Code formatting for file names, commands, paths, and code references
- Keep technical behaviour identical to the package. Do not invent features, flags, or deployer options.
- Internal links use Mintlify paths (`/drivers`, `/writing-a-driver`), not `docs/*.md`.

## Content boundaries

- Document the public API: config keys, commands, built-in steps, deployers, policies, drivers, and the four extension points.
- Do not document internal compiler internals beyond what users need to extend Slipway.
- Do not put secret values, real host keys, or production credentials in examples.
- Marketing copy and social posts live in the brand kit, not in these pages.
