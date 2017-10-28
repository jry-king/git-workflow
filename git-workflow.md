# A Brief Introduction to Git Workflow #

**Git Workflow** is the way people use Git to accomplish work in a consistent and productive manner. It involves the procedures of committing new files, making edits, solving conflicts, and so on. An effective workflow can significantly enhance the productivity of a software team. While one can personalize their own unique workflow, there are still some common patterns to learn.

## Centralized Workflow ##

![](https://wac-cdn.atlassian.com/dam/jcr:0869c664-5bc1-4bf2-bef0-12f3814b3187/01.svg?cdnVersion=ht)

Like svn, people can implement **Centralized Workflow** in Git. Centralized Workflow uses a central repository to serve as the single point-of-entry for all changes to the project, and it only uses a single branch called **master**. 

### How it works ###

![](https://wac-cdn.atlassian.com/dam/jcr:f03a0fbd-a880-477f-aa32-33340383ce07/02%20(3).svg?cdnVersion=ht)

Firstly, developers clone the central repository. Then they can edit files and commit changes locally, which allow them modify their files as many times as they want without affecting the central repository. When they finished editing, they can push their local master branch to the central repository.

### Managing Conflicts ###

![](https://wac-cdn.atlassian.com/dam/jcr:d06191e3-994e-453a-8ea9-a2e93374e53e/03%20(4).svg?cdnVersion=ht)

If a delevoper's local commit diverge from the central repository, Git will simple refuse to push this change. To solve this problem, developers need to clone the newest central repository then rebase their changes on top of them. If a merge conflict appears at this time, developer can solve it right away. In this way, they are changing what everyone else has done, making the workflow linear.

![](https://wac-cdn.atlassian.com/dam/jcr:5165668f-b62d-4417-95e6-fde8ed97ec60/11.svg?cdnVersion=ht)