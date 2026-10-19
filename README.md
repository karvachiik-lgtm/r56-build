# r56-build

CI-only. Builds the miner image from `karvachiik-lgtm/r56-threejs` at a **frozen commit**
and pushes to Docker Hub.

This repo exists so the submission repo is never modified: its HEAD SHA
(`527c8285...`) is committed on-chain for round 56, so any commit there would
invalidate the submission.

The image is for **our own generation run only** — the validator builds its own
image from the GitHub repo (`build.get_runnable_image()`) for the scored run and
all three audit repeats, and never pulls from Docker Hub.

Run: Actions -> build-miner-image -> Run workflow.
