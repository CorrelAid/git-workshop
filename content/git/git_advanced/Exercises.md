# Exercises

\[\[_TOC_\]\]

| Is this section core or elective? | Expected time to completion |
| --- | ---- |
| core | by the end of the first day |

Here are some practical exercises for you to try out. Remember to hand in a file with your bash commands as described in
[how to submit solutions.](../../Introduction#review-process-for-the-first-chapters-on-git)

1. Create at least two branches

1. Commit conflicting changes on two branches

1. Merge the two branches containing the conflicting changes

1. Use `git mergetool` ([meld](https://meldmerge.org/) recommended) to resolve
   the changes. Before `git mergetool` can be run, a mergetool like meld needs
   to be installed and configured.

   - Install Meld
     - Either install by downloading the Windows build from
       [meld](https://meldmerge.org) (minimum version: 3.20.3),
     - or install via [Chocolatey](https://chocolatey.org/install) running PowerShell as administrator:
       `choco install meld`
   - `git config --global merge.tool meld`
   - `git config --global mergetool.meld.path <path/to/Meld.exe>` The path can
     be provided in standard Windows path notation, but you need to replace backslashes
     with forward slashes (e.g. "C:/Users/dXXXXXX/AppData/Local/Programs/Meld/Meld.exe").

   The following commands should be run in the git project's folder:

   - `git config mergetool.meld.keepTemporaries false`
   - `git config mergetool.meld.keepBackup false`
   - `git config mergetool.meld.trustExitCode  false`
   - `git config mergetool.keepBackup false`

   The `--global` option allows you to configure meld for all git repositories
   you use, instead of just the current one, and is optional. If not used, the
   commands need to be run in the respective folder.

1. Commit the merge and view the history

## Navigation

- [Back to "Advanced Git"](./GitAdvanced)
- [Back to "Branches"](./Branches)
- [Back to "Merging"](./Merging)
