### Session 1 - 2026-02-01

#### Prompt (Developer)

look at 

https://github.com/podverse/podverse

on the develop branch

the podverse-monorepo repo needs a github action that is very similar to the "alpha" action on the podverse develop branch, except the end goal is to trigger this new action when code is pushed to the podcastdj-alpha branch, and it should use the Dockerfile.build.alpha-podverse.k.podcastdj.com and alpha-podverse.k.podcastdj.com.env and the end result of this action is to push an image to mitchdowney/web-deploy-podcastdj-alpha

Implement the plan as specified, it is attached for your reference. Do NOT edit the plan file itself.

To-do's from the plan have already been created. Do not create them again. Mark them as in_progress as you work, starting with the first one. Don't stop until you have completed all the to-dos.

#### Key Decisions

- Mirror `publish-alpha.yml` validation steps to keep parity with alpha deploy checks.
- Use `GHCR_MITCH_TOKEN` for GHCR tag lookup and publish to `ghcr.io/mitchdowney/web-deploy-podcastdj-alpha`.
- Build with `apps/web/Dockerfile.build.alpha-podverse.k.podcastdj.com` and bake in `apps/web/env/alpha-podverse.k.podcastdj.com.env`.

#### Files Modified

- .llm/history/active/podcastdj-alpha-workflow/podcastdj-alpha-workflow-part-01.md
- .github/workflows/publish-podcastdj-alpha.yml
