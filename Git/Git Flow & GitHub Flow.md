Git Flow and GitHub Flow are a kind of branch manage strategies. There are many different types of branch management strategies, but they use Git flow and Github flow a lot. 
# Why use branch management strategies?
There are various reasons for using branch management strategies, but they are usually used for maintenance. Below are the details.
### Cooperation efficiency
If you work in different branches, cooperation efficiency is increased and branch crashes are reduced. Namely, you can your work without interference.
### Ensuring stability
It is possible to manage codes that are experimental or have not yet been tested as separate branches.
### DevOps and CI / CD
DevOps can be realized by dividing branches to test and build CI/CD pipelines for deployment efficiently.
# Git Flow
![](https://images.squarespace-cdn.com/content/v1/5cd29903aadd34273bef66f8/50f3fcb5-5798-481c-85f0-5a85f0886ed9/Gitflow.png?format=2500w)           
Git Flow's structure promotes stability and predictability, making it well-suited for projects with scheduled releases. And Git Flow is also suitable for large-scale projects. 

Git Flow is divide into five major branches.
### Main branch
- the original branch from which the branch was derived
- also called "Master" Branch
- includes actual projects that can be commercialized, i.e. to be distributed (testing, quality control, etc.)
### Develop branch
- pre-production code with newly developed features being tested is included.
- it is similar to the main branch, but exists to branch into a release branch for testing or quality control, and a feature branch for feature development.
### Feature branch
- it's a branch to develop functions
- whenever you need to develop a feature, branch the feature branch
### Release branch
- it serves as a staging area for upcoming production releases. It focuses on final polishing and minor bug fixes specific to that release to ensure stable distribution.
- `Quality Assurance(QA)` is mainly carried out this branch.
### Hotfix branch
- branch for quick fixes to critical issues found in main branch
- it is created directly from the main branch and the changes are merged back into the main and develop branches once the modifications are complete.
# GitHub Flow
![](https://images.squarespace-cdn.com/content/v1/5cd29903aadd34273bef66f8/e05668eb-89fa-4ee0-8350-35c93d029fad/GitHub+Flow.png?format=2500w)
Github Flow is based on Github. And have a simple and efficient development flow.

Github Flow typically revolves around a single main branch (often referred to as "main" or "master") where production stores ready-to-use code. However, to develop features, we work by branching the feature branch from the main branch.

Github Flow is a simpler alternative to Git Flow, which is ideal for smaller teams because it does not require multiple versions to be managed.

Github Flow is flowing like this way.
make branch - commit - pull request - review & feedback - merge - distribute

In conclusion, Github flow is good at small scale projects and when have to fast distribute.

---
Reference link 🙂           
https://www.eisquare.co.uk/blogs/how-to-choose-your-branching-strategy#:~:text=GitFlow%3A%20A%20complex%20but%20structured,back%20into%20the%20main%20branch          
https://velog.io/@gmlstjq123/Git-Flow-VS-Github-Flow       