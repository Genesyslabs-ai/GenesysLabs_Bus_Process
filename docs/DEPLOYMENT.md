# Local development and supporting learning track

## Existing repository

Use the existing Git clone at `E:\Experiments\GenesysLabs\Bus-Model`, with remote `https://github.com/Genesyslabs-ai/GenesysLabs_Bus_Process.git`. Do not initialize another repository, replace its history or change the remote to match the old prototype's starter instructions.

The original `..\Bus-Oper-Model` and independent company-context clone `..\Shared-Context` remain separate. Application development belongs here; company-wide context is referenced rather than copied.

## Local preview

```powershell
Set-Location E:\Experiments\GenesysLabs\Bus-Model
python -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000>. Stop the server with Ctrl+C. The loopback binding keeps this development preview on the local machine. No framework, package installation or container is needed to use the app.

Export important browser-held edits before switching browser profile or origin. Browser storage is not Git-tracked or shared with other people.

## Review workflow

Inspect `git status` and `git diff` before reviewing changes. Ordinary `git diff` omits untracked additions, so review their contents and the full file inventory too. The current baseline integration has no staged changes or new commits.

Commit, merge, push and deployment require separate approval. Before a future authorized push, verify that `origin` still points to the intended repository and query current GitHub repository metadata to confirm private visibility. A private source repository does not provide authentication for a deployed application.

## Optional later Docker exercise

The copied `Dockerfile` and `compose.yaml` are unchanged V0.3 supporting material, not validated infrastructure. The Compose file publishes port 8080 without a loopback host restriction; review that binding before a future local exercise. Do not start containers during baseline integration.

Docker, CI/CD and authenticated hosting are later learning milestones after the business model and app review loop are usable. No hosting or CI pipeline has been configured here. Deployment would need a separate design and explicit authorization, including appropriate access control for internal material.
