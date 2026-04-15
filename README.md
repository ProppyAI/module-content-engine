# module-content-engine

HARNESS module: AI-powered content generation and document rendering.

## Entity Contract

- **Produces:** content-asset
- **Consumes:** client, job, estimate

## Tools

| Tool | Description |
|------|-------------|
| generate-image | Generate a branded image using NanoBanana Pro |
| generate-video | Generate a video using Seedance or Kling |
| generate-voiceover | Generate voice narration using CSM-1B |
| render-proposal | Render a branded proposal PDF from an estimate |
| render-invoice | Render a branded invoice PDF |

## fal.ai Integration

Content generation routes to fal.ai models via MCP integration:

- **Images:** NanoBanana Pro (`fal-ai/nano-banana-pro`)
- **Video:** Seedance (`fal-ai/seedance-1-0-pro`)
- **Voiceover:** CSM-1B (`fal-ai/csm-1b`)

## Hooks

- `PostJobCompleted` -> `auto-generate-completion-photo`: Automatically generates a completion photo when a job is marked complete.

## Setup

Bootstrap with HARNESS:

```bash
HARNESS_LOCAL=/path/to/HARNESS bash /path/to/HARNESS/bin/harness-init
```
