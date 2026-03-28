# Daily Memory - 2026-03-28

- Read `C:\Users\25472\Desktop\需求.md` and `C:\Users\25472\Desktop\3.28已经分割好的任务.md` before starting work.
- Active repository: `C:\Users\25472\projects\methods\mokaoai.com-private-upload`
- Task inbox: `task-todo/`
- Task done archive: `task-done/`
- In-progress status file: `task-in-progress\task-status.json`
- QQ progress target: `qqbot:c2c:4193BD194E319F7E000AF005F82E06CE`
- On new sessions, read this file first.
- 05:00 Heartbeat resumed the 2019 subject-sample PDF verification task. It confirmed that `schema-upgrade-copy/experiment-pdfs/2019-subject-sample/manifest.json` exists, includes 23 subject PDFs, and that `marker-pdf 1.10.2` plus `marker_single --help` are available.
- 05:01 `task-status.json` was corrupted by encoding damage, which can break `heartbeat-primary.ps1` and cause the task loop to stop early. The file has been rewritten as clean UTF-8 JSON and needs a watchdog layer.
- 11:08 Resumed the 2019 subject-sample PDF verification task. Confirmed the sample folder still only contains 23 PDFs plus `manifest.json` and no generated page-level artifacts yet. Verified `marker_single` usage, then started the first real conversion on the 2019 Calculus BC sample targeting `schema-upgrade-copy/experiment-pdfs/2019-subject-sample/outputs`; marker is currently bootstrapping by downloading its initial layout model before artifact inspection can continue.
- 11:11 Re-read the requirement/task context and checked the live marker conversion again. The `marker_single` / Python worker for the 2019 Calculus BC sample is still active with sustained CPU usage, but `schema-upgrade-copy/experiment-pdfs/2019-subject-sample/outputs` is still empty, so the next checkpoint is to wait for the first markdown/image artifacts and then document the produced structure.
- 11:20 Re-read the canonical requirement and split-task files from the desktop aliases, then checked the active conversion state again. The 11:02 `marker_single` / `python.exe` pair for the 2019 Calculus BC sample is still running, and `schema-upgrade-copy/experiment-pdfs/2019-subject-sample/outputs` still has no emitted files yet, so the task remains blocked on first artifact generation rather than needing a new source edit.
