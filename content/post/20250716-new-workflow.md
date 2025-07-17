---
title: "New Workflow Test WTF"
date: 2025-07-16T22:31:46-05:00
draft: false
Tags: ["Github Pages", "Self Hosting", "Git"]
---

If this post actually gets posted it means that my new workflow actually works. Apparently people far smarter than I am have already figured out a better way of
hosting Hugo websites through github pages. If I am reading the [documentation](https://gohugo.io/host-and-deploy/host-on-github-pages/) correctly all I will 
have to do is write my post, commit it to the Github Pages repository and then push those changes to Github. I won't even need to run hugo build.

Yep, this post is literally just exists for me to test that theory. Here goes nothing!


Ok, so that seems to have been a failure. lets try doing a hugo build and see if that works.

Nope. I have no clue what's going on. Lets sleep on it and see if I can figure a solution.

Figured it out. I goofed up my site configuration, and as a result new pages weren't building. Now I just need to move this branch to main. I think that may be a future me problem.

So, how does this work?

- First, we are now working out of the Github Pages repository. Not my personal git server repository.
- We do out pull request to avoid creating problems
- Then we create our new post same as usual.
- Once the post is finished and saved, we do a `git commit -am "I am a fancy message"` followed by a `git push`

That's it. Setting this up was just a matter of following the instructions in the documentation I linked earlier. All I did was change the branch as I wasn't quite sure it would work.

Once I do the `git push` Github apparently spins up a VM for the sole purpose of running `hugo build`. It then starts serving the newly built website.
Pretty slick but it does seem like MS is wasting a lot of compute resources to do that.
