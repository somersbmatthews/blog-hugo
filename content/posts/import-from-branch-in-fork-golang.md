---
title: "Import From Branch in Golang Version 1.15"
date: 2021-01-19T13:51:45-06:00
draft: true
---

For go version 1.15.5:

Step 0.) Make sure you there is a go.mod and go.sum in the repo to which you wish to import. If not there, run go mod init.

Step 1.) Go to the directory of your forked repository and checkout the branch you want.

Step 2.) Run the command: git log

Step 3.) Find the SHA of the commit you want to use and copy the first 8 or so characters from it.

FAQ: What is a SHA? Answer: It's the funny string after "commit" in your git log output that looks like this: commit 2f5162d937c6e66bd1f2b01f9dc86fd25b2857ec . You only need the first several characters.
 
Step 4.) In the directory of where you want to import into. Run the command 'go get "(regular import signature, you know how this works) github.com/somersbmatthews/mypackage@SHA"' where SHA is what you copied in step 3.

Step 5.) Your import in your code should import from the branch in step one without the @SHA.

Step 6.) To go change the branch back to master, run the go get command in step 4 without the @SHA part.


Below is the demonstration of the prescribed steps to importing branch code from a repository.

github.com/somersbmatthews/testy has a package called testy that contains a function testy.Run() which prints a string indicating whether or not you are in master or a branch.

I created a directory called "importdemo" in my ~/go/src/github.com/somersbmatthews directory, where somersbmatthews is my github name.

