
## Instructions (macOS)

#### Add remote GitHub repo to local directory (on macOS device)

#### Pull updates from remote GitHub repo directory to local GitHub repo directory (repo clone on macOS device)
* open Terminal app on macOS device
* type "cd" + spacebar then enter (changes directory to home directory)
* type "cd" + "path to local GitHub repo clone" (changes directory to local Github repo directory)
* type "git pull" (updates local GitHub repo directory with changes from remote Github repo directory)

#### Push updates from local GitHub directory to remote GitHub directory
use Git add (Method 1)
* type "cd" + <path_to_file_directory> (changes directory to specific directory containing created/updated file(s))
* type "git add [filename]" (selects file & moves it to staging area for next commit)
* type "git commit -a -m <'msg'>" (commit all changed files, <'msg'> as commit message)
* type "git push" (update remote GitHub directory from changes in local Github directory)
