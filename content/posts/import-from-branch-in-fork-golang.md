---
title: "Import From Branch in Fork Golang"
date: 2021-01-19T13:51:45-06:00
draft: true
---

Step 1.) Go to the directory of your forked repository and checkout the branch you want.

Step 2.) Run the command: git status

Step 3.) Find the SHA of the latest commit and copy it.

Step 4.) In the directory of where you want to import into. Run the command 'go get "(regular import signature, you know how this works) github.com/somersbmatthews/mypackage@SHA"' where SHA is what you copied in step 3.

Step 5.) Your import in your code should import from the branch in step one without the @SHA.

Step 6.) To go change the branch back to master, run the go get command in step 4 without the @SHA part.