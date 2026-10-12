# aiswec stages, moved

**The stages now live at [aiswec/core](https://github.com/aiswec/core)**, the open source home of
AISWEC's engine. This copy is archived: it stays readable, so a project that still calls it keeps
running, but it gets no more fixes.

To move a project, change the `uses:` line in each of its three workflow files, for example:

```yaml
uses: aiswec/core/.github/workflows/stage-refine.yml@v2
```

A project set up through [Suite](https://aiswec.com/suite/) can do it in one click: open the
project's *Setup* and press *Update*.
