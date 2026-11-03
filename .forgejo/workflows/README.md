# Forgejo workflows

This directory holds no workflows on purpose. Forgejo reads only the first
workflow directory it finds (`.forgejo/workflows`, then `.gitea/workflows`,
then `.github/workflows`), so its presence stops Forgejo from running
`.github/workflows/metrics.yml`, which is written for GitHub Actions.

GitHub ignores this directory and keeps running the metrics workflow.
The profile and metrics decision is tracked in alcxyz/gitops#1752.
Delete this directory to let Forgejo run `.github/workflows` again.
