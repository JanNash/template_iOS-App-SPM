## Template setup

After creating a repository from this template and cloning it, there are four placeholders to be replaced:
- `DEVELOPERNAME`
- `CREATIONDATE`
- `ORGANIZATION`
- `PROJECTNAME`

`DEVELOPERNAME` and `CREATIONDATE` only occur in the three swift files (`AppDelegate.swift`, `SceneDelegate.swift`, `ViewController.swift`), 
ORGANIZATION is only used in the bundle identifier in the project settings, so these can be replaced manually.

---

To replace `PROJECTNAME` with the name you've chosen for your project, run
`./initial_setup <desired project name>` inside the root folder of the repository.

The script will not run unless `git config user.name` and `git config user.email` are set.

---

The `initial_setup` script will setup your project in 11 steps:
1. install `rename` and `ack` via homebrew (without updating homebrew)
2. replace all occurrences of `PROJECTNAME` in file and directory names with the supplied name (using `find` and `rename`)
3. replace all occurrences of `PROJECTNAME` inside files with the supplied name (using `ack` and `sed`)
4. overwrite this README (`mv PROJECT_README.md README.md`)
5. run the `setup` script (`./setup`)
6. run the `run_synx_and_xUnique` script twice
7. add all changes (`git add .`)
8. remove the LICENSE file (`git rm LICENSE`)
9. remove itself from the index (`git rm --cached "$0:P"`)
10. overwrite the initial commit (`git commit --amend --no-edit`)
11. after waiting 5 seconds, delete itself (`rm "$0:P"`)
