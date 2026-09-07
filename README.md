# Repository Standards example

A synthetic, working standards source for learning and verifying
[Repository Standards](https://github.com/lutzseverino/repo-standards).
It is based on the product's Mira service example and is not the maintainer's
personal standards or a claim of production operational readiness.

The `service` profile installs an exact `.editorconfig` and guides an agent to
write project-specific operational documentation. A repeat-safe Node.js fix
initializes an unverified status record; a separate check verifies required
runbook sections and status. The operations require Node.js 24. Review the
scripts before confirming adoption: they run as trusted code on your machine.

## Validate locally

With an installed compatible Repository Standards CLI:

```sh
repo-standards source validate . --json
```

The declared CLI compatibility range is `>=1.0.0 <2.0.0`. The product's README
explains installation from a packed artifact until its npm release is available.

## Inspect before adoption

```sh
repo-standards inspect --source https://github.com/lutzseverino/repo-standards-example \
  --standards-version v1.0.0 --profile service --project /path/to/project --json
```

Use the stable release tag `v1.0.0` and complete profile `service`. Inspection is read-only and
executes no source scripts. Adoption requires a separate explicit confirmation.
The `repo-standards` topic also makes published stable releases discoverable
through `repo-standards source search --json`.

## License

[MIT](LICENSE). Adoption retains the source license with the selected inputs.
