
westking@Alpha-MacBook-Pro gitaction % act -s GITHUB_TOKEN=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
[FirstWorkflow/build] 🚀  Start image=ghcr.io/catthehacker/ubuntu:act-latest
[FirstWorkflow/build]   🐳  docker pull image=ghcr.io/catthehacker/ubuntu:act-latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=ghcr.io/catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=ghcr.io/catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -m 0777 -p /var/run/act] user=root workdir=
[FirstWorkflow/build] ⭐  Run show enviroment variable
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/0] user= workdir=
| “::debug::workspace=/Users/westking/gitaction”
[FirstWorkflow/build]   💬  ::debug::repository=gansuboywy/GitAction
[FirstWorkflow/build]   💬  ::debug::env=
[FirstWorkflow/build]   💬  ::debug::ref=refs/heads/master
[FirstWorkflow/build]   💬  ::debug::token=***
[FirstWorkflow/build]   ✅  Success - show enviroment variable
[FirstWorkflow/build] ⭐  Run check out source branch
[FirstWorkflow/build]   ☁  git clone 'https://github.com/actions/checkout' # ref=v3
[FirstWorkflow/build]   🐳  docker cp src=/Users/westking/.cache/act/actions-checkout@v3/ dst=/var/run/act/actions/actions-checkout@v3/
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -p /var/run/act/actions/actions-checkout@v3/] user= workdir=
[FirstWorkflow/build]   🐳  docker exec cmd=[node /var/run/act/actions/actions-checkout@v3/dist/index.js] user= workdir=
[FirstWorkflow/build]   ❓  ::save-state name=isPost::true
[FirstWorkflow/build]   💬  ::debug::GITHUB_WORKSPACE = '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::qualified repository = 'gansuboywy/GitAction'
[FirstWorkflow/build]   💬  ::debug::ref = 'refs/heads/Dev'
[FirstWorkflow/build]   💬  ::debug::commit = 'undefined'
[FirstWorkflow/build]   💬  ::debug::clean = true
[FirstWorkflow/build]   💬  ::debug::fetch depth = 1
[FirstWorkflow/build]   💬  ::debug::lfs = false
[FirstWorkflow/build]   💬  ::debug::submodules = false
[FirstWorkflow/build]   💬  ::debug::recursive submodules = false
[FirstWorkflow/build]   💬  ::debug::Repository owner ID not found within GITHUB event info
[FirstWorkflow/build]   ❓  ::add-matcher::/run/act/actions/actions-checkout@v3/dist/problem-matcher.json
| Syncing repository: gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::group::Getting Git version info
| Working directory is '/Users/westking/gitaction/Dev'
[FirstWorkflow/build]   💬  ::debug::Getting git version
| [command]/usr/bin/git version
| git version 2.36.1
[FirstWorkflow/build]   💬  ::debug::Set git useragent to: git/2.36.1 (github-actions-checkout)
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ⚙  ***
| Temporarily overriding HOME='/tmp/d388787c-0de2-4597-89c1-38320fbf0223' before making global git config changes
| Adding repository directory to the temporary git global config as a safe directory
| [command]/usr/bin/git config --global --add safe.directory /Users/westking/gitaction/Dev
[FirstWorkflow/build]   ❓  ::save-state name=setSafeDirectory::true
[FirstWorkflow/build]   ❓  ::save-state name=repositoryPath::/Users/westking/gitaction/Dev
[FirstWorkflow/build]   ❓  ::group::Initializing the repository
| [command]/usr/bin/git init /Users/westking/gitaction/Dev
| hint: Using 'master' as the name for the initial branch. This default branch name
| hint: is subject to change. To configure the initial branch name to use in all
| hint: of your new repositories, which will suppress this warning, call:
| hint: 
| hint: 	git config --global init.defaultBranch <name>
| hint: 
| hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
| hint: 'development'. The just-created branch can be renamed via this command:
| hint: 
| hint: 	git branch -m <name>
| Initialized empty Git repository in /Users/westking/gitaction/Dev/.git/
| [command]/usr/bin/git remote add origin https://github.com/gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Disabling automatic garbage collection
| [command]/usr/bin/git config --local gc.auto 0
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Setting up auth
| [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
| [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
| [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Fetching the repository
| [command]/usr/bin/git -c protocol.version=2 fetch --no-tags --prune --progress --no-recurse-submodules --depth=1 origin +refs/heads/Dev:refs/remotes/origin/Dev
| remote: Enumerating objects: 15, done.        
remote: Counting objects: 100% (15/15), done.        
remote: Compressing objects: 100% (8/8), done.        
| remote: Total 15 (delta 0), reused 3 (delta 0), pack-reused 0        
| From https://github.com/gansuboywy/GitAction
|  * [new branch]      Dev        -> origin/Dev
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Determining the checkout info
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Checking out the ref
| [command]/usr/bin/git checkout --progress --force -B Dev refs/remotes/origin/Dev
| Switched to a new branch 'Dev'
| branch 'Dev' set up to track 'origin/Dev'.
[FirstWorkflow/build]   ❓  ::endgroup::
| [command]/usr/bin/git log -1 --format='%H'
| '0398dd854160dd8e569466d8f55b3a2d5062f70a'
[FirstWorkflow/build]   💬  ::debug::Unsetting HOME override
[FirstWorkflow/build]   ❓  ::remove-matcher owner=checkout-git::
[FirstWorkflow/build]   ✅  Success - check out source branch
[FirstWorkflow/build] ⭐  Run Fetch action
[FirstWorkflow/build]   ☁  git clone 'https://github.com/Rishabh510/Path-lister-action' # ref=master
[FirstWorkflow/build]   🐳  docker pull image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   ⚙  ::set-output:: path_count=4
[FirstWorkflow/build]   ⚙  ::set-output:: paths=Dev/src/main/java/resources//newFile.txt Dev/src/main/java/resources//application.properties Dev/src/main/java/resources//dev.txt Dev/src/main/java/resources//logback-spring.xml 
| Dev/src/main/java/resources//newFile.txt Dev/src/main/java/resources//application.properties Dev/src/main/java/resources//dev.txt Dev/src/main/java/resources//logback-spring.xml 
[FirstWorkflow/build]   ✅  Success - Fetch action
[FirstWorkflow/build] ⭐  Run Output results
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/3] user= workdir=
| Found 4 file(s) with this extension:
| Dev/src/main/java/resources//newFile.txt
| Dev/src/main/java/resources//application.properties
| Dev/src/main/java/resources//dev.txt
| Dev/src/main/java/resources//logback-spring.xml
[FirstWorkflow/build]   ✅  Success - Output results
[FirstWorkflow/build] ⭐  Run check out target branch
[FirstWorkflow/build]   ☁  git clone 'https://github.com/actions/checkout' # ref=v3
[FirstWorkflow/build]   🐳  docker cp src=/Users/westking/.cache/act/actions-checkout@v3/ dst=/var/run/act/actions/actions-checkout@v3/
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -p /var/run/act/actions/actions-checkout@v3/] user= workdir=
[FirstWorkflow/build]   🐳  docker exec cmd=[node /var/run/act/actions/actions-checkout@v3/dist/index.js] user= workdir=
[FirstWorkflow/build]   ❓  ::save-state name=isPost::true
[FirstWorkflow/build]   💬  ::debug::GITHUB_WORKSPACE = '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::qualified repository = 'gansuboywy/GitAction'
[FirstWorkflow/build]   💬  ::debug::ref = 'refs/heads/master'
[FirstWorkflow/build]   💬  ::debug::commit = 'undefined'
[FirstWorkflow/build]   💬  ::debug::clean = true
[FirstWorkflow/build]   💬  ::debug::fetch depth = 1
[FirstWorkflow/build]   💬  ::debug::lfs = false
[FirstWorkflow/build]   💬  ::debug::submodules = false
[FirstWorkflow/build]   💬  ::debug::recursive submodules = false
[FirstWorkflow/build]   💬  ::debug::Repository owner ID not found within GITHUB event info
[FirstWorkflow/build]   ❓  ::add-matcher::/run/act/actions/actions-checkout@v3/dist/problem-matcher.json
| Syncing repository: gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::group::Getting Git version info
| Working directory is '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::Getting git version
| [command]/usr/bin/git version
| git version 2.36.1
[FirstWorkflow/build]   💬  ::debug::Set git useragent to: git/2.36.1 (github-actions-checkout)
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ⚙  ***
| Temporarily overriding HOME='/tmp/eb157223-7615-46ec-ba32-037a5254856a' before making global git config changes
| Adding repository directory to the temporary git global config as a safe directory
| [command]/usr/bin/git config --global --add safe.directory /Users/westking/gitaction
[FirstWorkflow/build]   ❓  ::save-state name=setSafeDirectory::true
| Deleting the contents of '/Users/westking/gitaction'
[FirstWorkflow/build]   ❓  ::save-state name=repositoryPath::/Users/westking/gitaction
[FirstWorkflow/build]   ❓  ::group::Initializing the repository
| [command]/usr/bin/git init /Users/westking/gitaction
| hint: Using 'master' as the name for the initial branch. This default branch name
| hint: is subject to change. To configure the initial branch name to use in all
| hint: of your new repositories, which will suppress this warning, call:
| hint: 
| hint: 	git config --global init.defaultBranch <name>
| hint: 
| hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
| hint: 'development'. The just-created branch can be renamed via this command:
| hint: 
| hint: 	git branch -m <name>
| Initialized empty Git repository in /Users/westking/gitaction/.git/
| [command]/usr/bin/git remote add origin https://github.com/gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Disabling automatic garbage collection
| [command]/usr/bin/git config --local gc.auto 0
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Setting up auth
| [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
| [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
| [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Fetching the repository
| [command]/usr/bin/git -c protocol.version=2 fetch --no-tags --prune --progress --no-recurse-submodules --depth=1 origin +refs/heads/master:refs/remotes/origin/master
| remote: Enumerating objects: 13, done.        
remote: Counting objects: 100% (13/13), done.        
remote: Compressing objects: 100% (8/8), done.        
| remote: Total 13 (delta 0), reused 8 (delta 0), pack-reused 0        
| From https://github.com/gansuboywy/GitAction
|  * [new branch]      master     -> origin/master
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Determining the checkout info
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Checking out the ref
| [command]/usr/bin/git checkout --progress --force -B master refs/remotes/origin/master
| Reset branch 'master'
| branch 'master' set up to track 'origin/master'.
[FirstWorkflow/build]   ❓  ::endgroup::
| [command]/usr/bin/git log -1 --format='%H'
| 'bd51247f8218ae29a9009a087d4f421b21e68e3a'
[FirstWorkflow/build]   💬  ::debug::Unsetting HOME override
[FirstWorkflow/build]   ❓  ::remove-matcher owner=checkout-git::
[FirstWorkflow/build]   ✅  Success - check out target branch
[FirstWorkflow/build] ⭐  Run Fetch action
[FirstWorkflow/build]   ☁  git clone 'https://github.com/Rishabh510/Path-lister-action' # ref=master
[FirstWorkflow/build]   🐳  docker pull image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   ⚙  ::set-output:: path_count=45
[FirstWorkflow/build]   ⚙  ::set-output:: paths=/Users/westking/gitaction/README.md /Users/westking/gitaction/src/main/java/resources/application.properties /Users/westking/gitaction/src/main/java/resources/logback-spring.xml /Users/westking/gitaction/.git/shallow /Users/westking/gitaction/.git/description /Users/westking/gitaction/.git/HEAD /Users/westking/gitaction/.git/index /Users/westking/gitaction/.git/FETCH_HEAD /Users/westking/gitaction/.git/config /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462 /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391 /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9 /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9 /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73 /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6 /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712 /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf /Users/westking/gitaction/.git/hooks/commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-rebase.sample /Users/westking/gitaction/.git/hooks/update.sample /Users/westking/gitaction/.git/hooks/pre-push.sample /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample /Users/westking/gitaction/.git/hooks/applypatch-msg.sample /Users/westking/gitaction/.git/hooks/pre-receive.sample /Users/westking/gitaction/.git/hooks/push-to-checkout.sample /Users/westking/gitaction/.git/hooks/post-update.sample /Users/westking/gitaction/.git/hooks/pre-applypatch.sample /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-commit.sample /Users/westking/gitaction/.git/logs/HEAD /Users/westking/gitaction/.git/logs/refs/remotes/origin/master /Users/westking/gitaction/.git/logs/refs/heads/master /Users/westking/gitaction/.git/refs/remotes/origin/master /Users/westking/gitaction/.git/refs/heads/master /Users/westking/gitaction/.git/info/exclude /Users/westking/gitaction/.github/workflows/maven.txt /Users/westking/gitaction/.github/workflows/maven-publish.txt /Users/westking/gitaction/.github/workflows/blank.yml /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt 
| /Users/westking/gitaction/README.md /Users/westking/gitaction/src/main/java/resources/application.properties /Users/westking/gitaction/src/main/java/resources/logback-spring.xml /Users/westking/gitaction/.git/shallow /Users/westking/gitaction/.git/description /Users/westking/gitaction/.git/HEAD /Users/westking/gitaction/.git/index /Users/westking/gitaction/.git/FETCH_HEAD /Users/westking/gitaction/.git/config /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462 /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391 /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9 /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9 /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73 /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6 /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712 /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf /Users/westking/gitaction/.git/hooks/commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-rebase.sample /Users/westking/gitaction/.git/hooks/update.sample /Users/westking/gitaction/.git/hooks/pre-push.sample /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample /Users/westking/gitaction/.git/hooks/applypatch-msg.sample /Users/westking/gitaction/.git/hooks/pre-receive.sample /Users/westking/gitaction/.git/hooks/push-to-checkout.sample /Users/westking/gitaction/.git/hooks/post-update.sample /Users/westking/gitaction/.git/hooks/pre-applypatch.sample /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-commit.sample /Users/westking/gitaction/.git/logs/HEAD /Users/westking/gitaction/.git/logs/refs/remotes/origin/master /Users/westking/gitaction/.git/logs/refs/heads/master /Users/westking/gitaction/.git/refs/remotes/origin/master /Users/westking/gitaction/.git/refs/heads/master /Users/westking/gitaction/.git/info/exclude /Users/westking/gitaction/.github/workflows/maven.txt /Users/westking/gitaction/.github/workflows/maven-publish.txt /Users/westking/gitaction/.github/workflows/blank.yml /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt 
[FirstWorkflow/build]   ✅  Success - Fetch action
[FirstWorkflow/build] ⭐  Run Output results
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/6] user= workdir=
| Found 45 file(s) with this extension:
| /Users/westking/gitaction/README.md
| /Users/westking/gitaction/src/main/java/resources/application.properties
| /Users/westking/gitaction/src/main/java/resources/logback-spring.xml
| /Users/westking/gitaction/.git/shallow
| /Users/westking/gitaction/.git/description
| /Users/westking/gitaction/.git/HEAD
| /Users/westking/gitaction/.git/index
| /Users/westking/gitaction/.git/FETCH_HEAD
| /Users/westking/gitaction/.git/config
| /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462
| /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a
| /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391
| /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e
| /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9
| /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9
| /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe
| /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73
| /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6
| /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712
| /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a
| /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d
| /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf
| /Users/westking/gitaction/.git/hooks/commit-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-rebase.sample
| /Users/westking/gitaction/.git/hooks/update.sample
| /Users/westking/gitaction/.git/hooks/pre-push.sample
| /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample
| /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample
| /Users/westking/gitaction/.git/hooks/applypatch-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-receive.sample
| /Users/westking/gitaction/.git/hooks/push-to-checkout.sample
| /Users/westking/gitaction/.git/hooks/post-update.sample
| /Users/westking/gitaction/.git/hooks/pre-applypatch.sample
| /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-commit.sample
| /Users/westking/gitaction/.git/logs/HEAD
| /Users/westking/gitaction/.git/logs/refs/remotes/origin/master
| /Users/westking/gitaction/.git/logs/refs/heads/master
| /Users/westking/gitaction/.git/refs/remotes/origin/master
| /Users/westking/gitaction/.git/refs/heads/master
| /Users/westking/gitaction/.git/info/exclude
| /Users/westking/gitaction/.github/workflows/maven.txt
| /Users/westking/gitaction/.github/workflows/maven-publish.txt
| /Users/westking/gitaction/.github/workflows/blank.yml
| /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt
[FirstWorkflow/build]   ✅  Success - Output results
[FirstWorkflow/build] ⭐  Run copy file
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/7] user= workdir=
| /Users/westking/gitaction
| cp: cannot stat 'Dev/src/main/java/resources/': No such file or directory
[FirstWorkflow/build]   ❌  Failure - copy file
[FirstWorkflow/build] exit with `FAILURE`: 1
Error: Job 'build' failed
westking@Alpha-MacBook-Pro gitaction % act -s GITHUB_TOKEN=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
[FirstWorkflow/build] 🚀  Start image=ghcr.io/catthehacker/ubuntu:act-latest
[FirstWorkflow/build]   🐳  docker pull image=ghcr.io/catthehacker/ubuntu:act-latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=ghcr.io/catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=ghcr.io/catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -m 0777 -p /var/run/act] user=root workdir=
[FirstWorkflow/build] ⭐  Run show enviroment variable
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/0] user= workdir=
| “::debug::workspace=/Users/westking/gitaction”
[FirstWorkflow/build]   💬  ::debug::repository=gansuboywy/GitAction
[FirstWorkflow/build]   💬  ::debug::env=
[FirstWorkflow/build]   💬  ::debug::ref=refs/heads/master
[FirstWorkflow/build]   💬  ::debug::token=***
[FirstWorkflow/build]   ✅  Success - show enviroment variable
[FirstWorkflow/build] ⭐  Run check out source branch
[FirstWorkflow/build]   ☁  git clone 'https://github.com/actions/checkout' # ref=v3
[FirstWorkflow/build]   🐳  docker cp src=/Users/westking/.cache/act/actions-checkout@v3/ dst=/var/run/act/actions/actions-checkout@v3/
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -p /var/run/act/actions/actions-checkout@v3/] user= workdir=
[FirstWorkflow/build]   🐳  docker exec cmd=[node /var/run/act/actions/actions-checkout@v3/dist/index.js] user= workdir=
[FirstWorkflow/build]   ❓  ::save-state name=isPost::true
[FirstWorkflow/build]   💬  ::debug::GITHUB_WORKSPACE = '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::qualified repository = 'gansuboywy/GitAction'
[FirstWorkflow/build]   💬  ::debug::ref = 'refs/heads/Dev'
[FirstWorkflow/build]   💬  ::debug::commit = 'undefined'
[FirstWorkflow/build]   💬  ::debug::clean = true
[FirstWorkflow/build]   💬  ::debug::fetch depth = 1
[FirstWorkflow/build]   💬  ::debug::lfs = false
[FirstWorkflow/build]   💬  ::debug::submodules = false
[FirstWorkflow/build]   💬  ::debug::recursive submodules = false
[FirstWorkflow/build]   💬  ::debug::Repository owner ID not found within GITHUB event info
[FirstWorkflow/build]   ❓  ::add-matcher::/run/act/actions/actions-checkout@v3/dist/problem-matcher.json
| Syncing repository: gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::group::Getting Git version info
| Working directory is '/Users/westking/gitaction/Dev'
[FirstWorkflow/build]   💬  ::debug::Getting git version
| [command]/usr/bin/git version
| git version 2.36.1
[FirstWorkflow/build]   💬  ::debug::Set git useragent to: git/2.36.1 (github-actions-checkout)
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ⚙  ***
| Temporarily overriding HOME='/tmp/1dabb0fb-9c9f-4667-8e74-af6e11ea40d2' before making global git config changes
| Adding repository directory to the temporary git global config as a safe directory
| [command]/usr/bin/git config --global --add safe.directory /Users/westking/gitaction/Dev
[FirstWorkflow/build]   ❓  ::save-state name=setSafeDirectory::true
[FirstWorkflow/build]   ❓  ::save-state name=repositoryPath::/Users/westking/gitaction/Dev
[FirstWorkflow/build]   ❓  ::group::Initializing the repository
| [command]/usr/bin/git init /Users/westking/gitaction/Dev
| hint: Using 'master' as the name for the initial branch. This default branch name
| hint: is subject to change. To configure the initial branch name to use in all
| hint: of your new repositories, which will suppress this warning, call:
| hint: 
| hint: 	git config --global init.defaultBranch <name>
| hint: 
| hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
| hint: 'development'. The just-created branch can be renamed via this command:
| hint: 
| hint: 	git branch -m <name>
| Initialized empty Git repository in /Users/westking/gitaction/Dev/.git/
| [command]/usr/bin/git remote add origin https://github.com/gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Disabling automatic garbage collection
| [command]/usr/bin/git config --local gc.auto 0
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Setting up auth
| [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
| [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
| [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Fetching the repository
| [command]/usr/bin/git -c protocol.version=2 fetch --no-tags --prune --progress --no-recurse-submodules --depth=1 origin +refs/heads/Dev:refs/remotes/origin/Dev
| remote: Enumerating objects: 15, done.        
remote: Counting objects: 100% (15/15), done.        
remote: Compressing objects: 100% (8/8), done.        
| remote: Total 15 (delta 0), reused 3 (delta 0), pack-reused 0        
| From https://github.com/gansuboywy/GitAction
|  * [new branch]      Dev        -> origin/Dev
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Determining the checkout info
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Checking out the ref
| [command]/usr/bin/git checkout --progress --force -B Dev refs/remotes/origin/Dev
| Switched to a new branch 'Dev'
| branch 'Dev' set up to track 'origin/Dev'.
[FirstWorkflow/build]   ❓  ::endgroup::
| [command]/usr/bin/git log -1 --format='%H'
| '0398dd854160dd8e569466d8f55b3a2d5062f70a'
[FirstWorkflow/build]   💬  ::debug::Unsetting HOME override
[FirstWorkflow/build]   ❓  ::remove-matcher owner=checkout-git::
[FirstWorkflow/build]   ✅  Success - check out source branch
[FirstWorkflow/build] ⭐  Run Fetch action
[FirstWorkflow/build]   ☁  git clone 'https://github.com/Rishabh510/Path-lister-action' # ref=master
[FirstWorkflow/build]   🐳  docker pull image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   ⚙  ::set-output:: path_count=4
[FirstWorkflow/build]   ⚙  ::set-output:: paths=Dev/src/main/java/resources//newFile.txt Dev/src/main/java/resources//application.properties Dev/src/main/java/resources//dev.txt Dev/src/main/java/resources//logback-spring.xml 
| Dev/src/main/java/resources//newFile.txt Dev/src/main/java/resources//application.properties Dev/src/main/java/resources//dev.txt Dev/src/main/java/resources//logback-spring.xml 
[FirstWorkflow/build]   ✅  Success - Fetch action
[FirstWorkflow/build] ⭐  Run Output results
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/3] user= workdir=
| Found 4 file(s) with this extension:
| Dev/src/main/java/resources//newFile.txt
| Dev/src/main/java/resources//application.properties
| Dev/src/main/java/resources//dev.txt
| Dev/src/main/java/resources//logback-spring.xml
[FirstWorkflow/build]   ✅  Success - Output results
[FirstWorkflow/build] ⭐  Run check out target branch
[FirstWorkflow/build]   ☁  git clone 'https://github.com/actions/checkout' # ref=v3
[FirstWorkflow/build]   🐳  docker cp src=/Users/westking/.cache/act/actions-checkout@v3/ dst=/var/run/act/actions/actions-checkout@v3/
[FirstWorkflow/build]   🐳  docker exec cmd=[mkdir -p /var/run/act/actions/actions-checkout@v3/] user= workdir=
[FirstWorkflow/build]   🐳  docker exec cmd=[node /var/run/act/actions/actions-checkout@v3/dist/index.js] user= workdir=
[FirstWorkflow/build]   ❓  ::save-state name=isPost::true
[FirstWorkflow/build]   💬  ::debug::GITHUB_WORKSPACE = '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::qualified repository = 'gansuboywy/GitAction'
[FirstWorkflow/build]   💬  ::debug::ref = 'refs/heads/master'
[FirstWorkflow/build]   💬  ::debug::commit = 'undefined'
[FirstWorkflow/build]   💬  ::debug::clean = true
[FirstWorkflow/build]   💬  ::debug::fetch depth = 1
[FirstWorkflow/build]   💬  ::debug::lfs = false
[FirstWorkflow/build]   💬  ::debug::submodules = false
[FirstWorkflow/build]   💬  ::debug::recursive submodules = false
[FirstWorkflow/build]   💬  ::debug::Repository owner ID not found within GITHUB event info
[FirstWorkflow/build]   ❓  ::add-matcher::/run/act/actions/actions-checkout@v3/dist/problem-matcher.json
| Syncing repository: gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::group::Getting Git version info
| Working directory is '/Users/westking/gitaction'
[FirstWorkflow/build]   💬  ::debug::Getting git version
| [command]/usr/bin/git version
| git version 2.36.1
[FirstWorkflow/build]   💬  ::debug::Set git useragent to: git/2.36.1 (github-actions-checkout)
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ⚙  ***
| Temporarily overriding HOME='/tmp/3518d55c-5c16-4dc6-bf6d-690429a38caf' before making global git config changes
| Adding repository directory to the temporary git global config as a safe directory
| [command]/usr/bin/git config --global --add safe.directory /Users/westking/gitaction
[FirstWorkflow/build]   ❓  ::save-state name=setSafeDirectory::true
| Deleting the contents of '/Users/westking/gitaction'
[FirstWorkflow/build]   ❓  ::save-state name=repositoryPath::/Users/westking/gitaction
[FirstWorkflow/build]   ❓  ::group::Initializing the repository
| [command]/usr/bin/git init /Users/westking/gitaction
| hint: Using 'master' as the name for the initial branch. This default branch name
| hint: is subject to change. To configure the initial branch name to use in all
| hint: of your new repositories, which will suppress this warning, call:
| hint: 
| hint: 	git config --global init.defaultBranch <name>
| hint: 
| hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
| hint: 'development'. The just-created branch can be renamed via this command:
| hint: 
| hint: 	git branch -m <name>
| Initialized empty Git repository in /Users/westking/gitaction/.git/
| [command]/usr/bin/git remote add origin https://github.com/gansuboywy/GitAction
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Disabling automatic garbage collection
| [command]/usr/bin/git config --local gc.auto 0
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Setting up auth
| [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
| [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
| [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
| [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Fetching the repository
| [command]/usr/bin/git -c protocol.version=2 fetch --no-tags --prune --progress --no-recurse-submodules --depth=1 origin +refs/heads/master:refs/remotes/origin/master
| remote: Enumerating objects: 13, done.        
remote: Counting objects: 100% (13/13), done.        
remote: Compressing objects: 100% (8/8), done.        
| remote: Total 13 (delta 0), reused 8 (delta 0), pack-reused 0        
| From https://github.com/gansuboywy/GitAction
|  * [new branch]      master     -> origin/master
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Determining the checkout info
[FirstWorkflow/build]   ❓  ::endgroup::
[FirstWorkflow/build]   ❓  ::group::Checking out the ref
| [command]/usr/bin/git checkout --progress --force -B master refs/remotes/origin/master
| Reset branch 'master'
| branch 'master' set up to track 'origin/master'.
[FirstWorkflow/build]   ❓  ::endgroup::
| [command]/usr/bin/git log -1 --format='%H'
| 'bd51247f8218ae29a9009a087d4f421b21e68e3a'
[FirstWorkflow/build]   💬  ::debug::Unsetting HOME override
[FirstWorkflow/build]   ❓  ::remove-matcher owner=checkout-git::
[FirstWorkflow/build]   ✅  Success - check out target branch
[FirstWorkflow/build] ⭐  Run Fetch action
[FirstWorkflow/build]   ☁  git clone 'https://github.com/Rishabh510/Path-lister-action' # ref=master
[FirstWorkflow/build]   🐳  docker pull image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= username= forcePull=false
[FirstWorkflow/build]   🐳  docker create image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   🐳  docker run image=act-rishabh510-path-lister-action-master-dockeraction:latest platform= entrypoint=[] cmd=[]
[FirstWorkflow/build]   ⚙  ::set-output:: path_count=45
[FirstWorkflow/build]   ⚙  ::set-output:: paths=/Users/westking/gitaction/README.md /Users/westking/gitaction/src/main/java/resources/application.properties /Users/westking/gitaction/src/main/java/resources/logback-spring.xml /Users/westking/gitaction/.git/shallow /Users/westking/gitaction/.git/description /Users/westking/gitaction/.git/HEAD /Users/westking/gitaction/.git/index /Users/westking/gitaction/.git/FETCH_HEAD /Users/westking/gitaction/.git/config /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462 /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391 /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9 /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9 /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73 /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6 /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712 /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf /Users/westking/gitaction/.git/hooks/commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-rebase.sample /Users/westking/gitaction/.git/hooks/update.sample /Users/westking/gitaction/.git/hooks/pre-push.sample /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample /Users/westking/gitaction/.git/hooks/applypatch-msg.sample /Users/westking/gitaction/.git/hooks/pre-receive.sample /Users/westking/gitaction/.git/hooks/push-to-checkout.sample /Users/westking/gitaction/.git/hooks/post-update.sample /Users/westking/gitaction/.git/hooks/pre-applypatch.sample /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-commit.sample /Users/westking/gitaction/.git/logs/HEAD /Users/westking/gitaction/.git/logs/refs/remotes/origin/master /Users/westking/gitaction/.git/logs/refs/heads/master /Users/westking/gitaction/.git/refs/remotes/origin/master /Users/westking/gitaction/.git/refs/heads/master /Users/westking/gitaction/.git/info/exclude /Users/westking/gitaction/.github/workflows/maven.txt /Users/westking/gitaction/.github/workflows/maven-publish.txt /Users/westking/gitaction/.github/workflows/blank.yml /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt 
| /Users/westking/gitaction/README.md /Users/westking/gitaction/src/main/java/resources/application.properties /Users/westking/gitaction/src/main/java/resources/logback-spring.xml /Users/westking/gitaction/.git/shallow /Users/westking/gitaction/.git/description /Users/westking/gitaction/.git/HEAD /Users/westking/gitaction/.git/index /Users/westking/gitaction/.git/FETCH_HEAD /Users/westking/gitaction/.git/config /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462 /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391 /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9 /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9 /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73 /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6 /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712 /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf /Users/westking/gitaction/.git/hooks/commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-rebase.sample /Users/westking/gitaction/.git/hooks/update.sample /Users/westking/gitaction/.git/hooks/pre-push.sample /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample /Users/westking/gitaction/.git/hooks/applypatch-msg.sample /Users/westking/gitaction/.git/hooks/pre-receive.sample /Users/westking/gitaction/.git/hooks/push-to-checkout.sample /Users/westking/gitaction/.git/hooks/post-update.sample /Users/westking/gitaction/.git/hooks/pre-applypatch.sample /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample /Users/westking/gitaction/.git/hooks/pre-commit.sample /Users/westking/gitaction/.git/logs/HEAD /Users/westking/gitaction/.git/logs/refs/remotes/origin/master /Users/westking/gitaction/.git/logs/refs/heads/master /Users/westking/gitaction/.git/refs/remotes/origin/master /Users/westking/gitaction/.git/refs/heads/master /Users/westking/gitaction/.git/info/exclude /Users/westking/gitaction/.github/workflows/maven.txt /Users/westking/gitaction/.github/workflows/maven-publish.txt /Users/westking/gitaction/.github/workflows/blank.yml /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt 
[FirstWorkflow/build]   ✅  Success - Fetch action
[FirstWorkflow/build] ⭐  Run Output results
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/6] user= workdir=
| Found 45 file(s) with this extension:
| /Users/westking/gitaction/README.md
| /Users/westking/gitaction/src/main/java/resources/application.properties
| /Users/westking/gitaction/src/main/java/resources/logback-spring.xml
| /Users/westking/gitaction/.git/shallow
| /Users/westking/gitaction/.git/description
| /Users/westking/gitaction/.git/HEAD
| /Users/westking/gitaction/.git/index
| /Users/westking/gitaction/.git/FETCH_HEAD
| /Users/westking/gitaction/.git/config
| /Users/westking/gitaction/.git/objects/e5/a5ee57d0fecef5c22e06afd9f6e6ad12549462
| /Users/westking/gitaction/.git/objects/bd/51247f8218ae29a9009a087d4f421b21e68e3a
| /Users/westking/gitaction/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391
| /Users/westking/gitaction/.git/objects/f4/46491b18f69cdeee27f192badc04ef6fec023e
| /Users/westking/gitaction/.git/objects/3b/6236a6f76f0f852ad60679e1cbd08bfc350ba9
| /Users/westking/gitaction/.git/objects/00/92139aa1ede4e317c0acb07f3513f7d9b273c9
| /Users/westking/gitaction/.git/objects/8e/7f21e4bb9bf20d7c52bf1e9c61e3026beb6bbe
| /Users/westking/gitaction/.git/objects/da/b69fef79141c2f940c67de518c2c2564d1da73
| /Users/westking/gitaction/.git/objects/c6/f4b82be65817957aa9cb9e1209ceccc975b0c6
| /Users/westking/gitaction/.git/objects/78/db6d2a31db3dbeffc567adac7c1aee2ec05712
| /Users/westking/gitaction/.git/objects/84/ebc59c430868fa01350bc1e3db28a3380fac9a
| /Users/westking/gitaction/.git/objects/6e/405df661bd727a730828764d94171e1aaa5c8d
| /Users/westking/gitaction/.git/objects/1d/3f6592bbdfa9fe6348b5bcd3b59f2d42126acf
| /Users/westking/gitaction/.git/hooks/commit-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-rebase.sample
| /Users/westking/gitaction/.git/hooks/update.sample
| /Users/westking/gitaction/.git/hooks/pre-push.sample
| /Users/westking/gitaction/.git/hooks/fsmonitor-watchman.sample
| /Users/westking/gitaction/.git/hooks/pre-merge-commit.sample
| /Users/westking/gitaction/.git/hooks/applypatch-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-receive.sample
| /Users/westking/gitaction/.git/hooks/push-to-checkout.sample
| /Users/westking/gitaction/.git/hooks/post-update.sample
| /Users/westking/gitaction/.git/hooks/pre-applypatch.sample
| /Users/westking/gitaction/.git/hooks/prepare-commit-msg.sample
| /Users/westking/gitaction/.git/hooks/pre-commit.sample
| /Users/westking/gitaction/.git/logs/HEAD
| /Users/westking/gitaction/.git/logs/refs/remotes/origin/master
| /Users/westking/gitaction/.git/logs/refs/heads/master
| /Users/westking/gitaction/.git/refs/remotes/origin/master
| /Users/westking/gitaction/.git/refs/heads/master
| /Users/westking/gitaction/.git/info/exclude
| /Users/westking/gitaction/.github/workflows/maven.txt
| /Users/westking/gitaction/.github/workflows/maven-publish.txt
| /Users/westking/gitaction/.github/workflows/blank.yml
| /Users/westking/gitaction/.github/workflows/azure-webapps-java-jar.txt
[FirstWorkflow/build]   ✅  Success - Output results
[FirstWorkflow/build] ⭐  Run copy file
[FirstWorkflow/build]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/7] user= workdir=
| /Users/westking/gitaction
| cp: cannot stat 'Dev/src/main/java/resources/': No such file or directory
[FirstWorkflow/build]   ❌  Failure - copy file
[FirstWorkflow/build] exit with `FAILURE`: 1