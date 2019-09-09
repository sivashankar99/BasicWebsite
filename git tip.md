Configuring a remote for a fork
You must configure a remote that points to the upstream repository in Git to sync changes you make in a fork with the original repository. This also allows you to sync changes made in the original repository with the fork.

List the current configured remote repository for your fork.
``` shell
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git remote -v
origin	https://sivashan9@bitbucket.org/sivashan9/isiva-philips-idm-portal-2.git (fetch)
origin	https://sivashan9@bitbucket.org/sivashan9/isiva-philips-idm-portal-2.git (push)
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git remote add upstream https://sivashan9@bitbucket.org/phi_hydra/philips-idm-portal.git
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git remote -v
origin	https://sivashan9@bitbucket.org/sivashan9/isiva-philips-idm-portal-2.git (fetch)
origin	https://sivashan9@bitbucket.org/sivashan9/isiva-philips-idm-portal-2.git (push)
upstream	https://sivashan9@bitbucket.org/phi_hydra/philips-idm-portal.git (fetch)
upstream	https://sivashan9@bitbucket.org/phi_hydra/philips-idm-portal.git (push)
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git fetch upstream
Password for 'https://sivashan9@bitbucket.org': 
remote: Counting objects: 80, done.
remote: Compressing objects: 100% (72/72), done.
remote: Total 80 (delta 62), reused 16 (delta 7)
Unpacking objects: 100% (80/80), done.
From https://bitbucket.org/phi_hydra/philips-idm-portal
 * [new branch]          C7-Develop                                 -> upstream/C7-Develop
 * [new branch]          C7-Release                                 -> upstream/C7-Release
 * [new branch]          develop                                    -> upstream/develop
 * [new branch]          eis                                        -> upstream/eis
 * [new branch]          master                                     -> upstream/master
 * [new branch]          release                                    -> upstream/release
 * [new branch]          release123                                 -> upstream/release123
 * [new branch]          revert-pr-299                              -> upstream/revert-pr-299
 * [new branch]          versioning                                 -> upstream/versioning
 * [new tag]             idm_portal_release_build_1_12_0_0_20190726 -> idm_portal_release_build_1_12_0_0_20190726
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git checkout release
Already on 'release'
Your branch is ahead of 'origin/release' by 6 commits.
  (use "git push" to publish your local commits)
philips@philips-HP-EliteDesk-800-G3-TWR:~/isiva-philips-idm-portal-2$ git merge upstream/release
Already up to date. 
```
