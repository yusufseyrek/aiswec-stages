# aiswec stages

The three stage workflows of [AISWEC](https://aiswec.com), the AI software engineer for GitHub:
refine (an issue becomes a plan), build (an approved plan becomes a pull request) and revise
(review feedback becomes a reply and commits). A project calls them from three small workflow
files of its own, which Suite writes when it sets a project up:

```yaml
jobs:
  refine:
    uses: yusufseyrek/aiswec-stages/.github/workflows/stage-refine.yml@v2
    secrets:
      claude_code_oauth_token: ${{ secrets.CLAUDE_CODE_OAUTH_TOKEN }}
      openrouter_api_key: ${{ secrets.OPENROUTER_API_KEY }}
      aiswec_app_id: ${{ secrets.AISWEC_APP_ID }}
    with:
      namespace: aiswec
```

This repository is a published copy, not the source. The stages are developed in a private
repository and written here by its deploy on every release, with `v2` moved to the same commit,
so a pull request or an issue opened here is not read. The manual is at
[aiswec.com/suite/docs](https://aiswec.com/suite/docs); questions go to hello@aiswec.com.
