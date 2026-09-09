# Repository Standards example

A synthetic, working standards source for learning and verifying
[Repository Standards](https://github.com/lutzseverino/repo-standards).
It brings the product's synthetic Mira and Alice examples together in one public
repository. These are two complete profiles of one standards source, not two
independent public publishers. They are not the maintainer's personal standards
or a claim of production operational readiness.

The `service` profile installs an exact `.editorconfig` and guides an agent to
write project-specific operational documentation. A repeat-safe Node.js fix
initializes an unverified status record; a separate check verifies required
runbook sections and status. The operations require Node.js 24. Review the
scripts before confirming adoption: they run as trusted code on your machine.

The `work` profile selects Alice's work-specific `AGENTS.md`, exact review skill,
README guidance and source-layout guidance. It excludes contribution guidance,
preserving the adopting project's employer-owned `CONTRIBUTING.md`, and excludes
Mira's declarations. Its README heading check requires Python >=3.12,<4.
The `service` profile excludes Alice's declarations and retains its original
Mira material. Defaults and explicit profile exclusions keep each selection
complete without cross-profile inheritance.

## Validate locally

With an installed compatible Repository Standards CLI:

```sh
repo-standards source validate . --json
```

The declared CLI compatibility range is `>=1.0.0 <2.0.0`. See the product's
[public installation instructions](https://github.com/lutzseverino/repo-standards/blob/main/docs/installation.md).
Commands require a compatible published CLI version.

## Inspect before adoption

```sh
repo-standards inspect --source https://github.com/lutzseverino/repo-standards-example \
  --standards-version v1.1.0 --profile service --project /path/to/project --json
```

Use stable release tag `v1.1.0` and complete profile `service` or `work`.
The original service-only `v1.0.0` release remains unchanged. Inspection is read-only and
executes no source scripts. Adoption requires a separate explicit confirmation.
The `repo-standards` topic also makes published stable releases discoverable
through `repo-standards source search --json`.

## License

[MIT](LICENSE). Adoption retains the source license with the selected inputs.
