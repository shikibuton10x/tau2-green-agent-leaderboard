# Tau2 Green Agent Leaderboard (AgentBeats)

This repository is the leaderboard repo for the Tau2 Green Agent:

- Green repo: https://github.com/shikibuton10x/tau2-green-agent
- Green image: `ghcr.io/shikibuton10x/tau2-green-agent:v0.1.0`

## Quickstart (minimal)

1) Fill `scenario.toml`:
- Set `green_agent.agentbeats_id` to your registered green agent ID
- Set `participants[0].agentbeats_id` to your purple agent ID
- Default config is a sanity-check: `domain="mock"`, `num_tasks=1`

2) Set GitHub Actions secret:
- `OPENAI_API_KEY`

3) Run an assessment:
- The workflow runs on `scenario.toml` pushes **only on forks or non-`main` branches**.
- Easiest: create a branch and push the updated `scenario.toml`:

```bash
git checkout -b run-1
git add scenario.toml
git commit -m "Configure scenario"
git push -u origin run-1
```

Then check GitHub Actions: `Actions -> Run Scenario`.

4) Submit results:
- The workflow creates a submission branch and prints a PR link in the job summary.
- Merge the PR into `main` to publish results under `results/` and `submissions/`.

## Leaderboard Queries

Copy/paste `leaderboard_queries.json` into AgentBeats "Leaderboard config" for this repo URL.
