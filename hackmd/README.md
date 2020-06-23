# GitHub Documents powered by HackMD

[ Versions:
[Published](https://github.com/mhevery/sandbox/blob/master/hackmd/README.md) | 
[Working Copy](https://hackmd.io/@mhevery/Byaksnk08) ]

This page is a demonstration of how HackMD and GitHub can work together.

## Goals

Each setup has different trade-offs between different benefits which the people find of value for their workflow. This setups goals are:

- *Published*: A set of goals to make the document easy to discover and consume by the community.
    - GitHub is the source of truth and final record of the documents.
        - We need a separate repo where we store these documents, so that we don't have to have CI, and complex pull-request process. (Ideally this would be the repo's wiki, but that is not yet supported.)
    - A document can always be accessed by its public URL [Simply the URL pointing to the document in the GitHub repo]
- *Working Copy*: A set of goals to make creation and collaborations of the documents easy.
    - HackMD integration for creating, updating, and discussing the documents.
    - All work is done on HackMD, which has a collaborative UI for editing and commenting.
    - All discussion is performed on the HackMD which supports comments, threads, and resolution.
    - Periodically pushing the document from the working HackMD to the GitHub aka "Publishing".

## URLs

Each document has two URLs. The "published" URL which points to the GitHub. (In this document case it would be https://github.com/mhevery/sandbox/blob/master/hackmd/README.md). And a HackMD document where all of the creation, editing, and discussion happens. (In this document it would be https://hackmd.io/@mhevery/Byaksnk08). The two URLs would be know as [Published](https://github.com/mhevery/sandbox/blob/master/hackmd/README.md) and 
[Working Copy](https://hackmd.io/@mhevery/Byaksnk08) respectively.

As a best practice each document should include the two links at the top of the document to make navigation and discovery easier. It is expected that the author of the document creates these links on first time publish.

Example of links at the top of the document:
> [ Versions:
[Published](https://github.com/mhevery/sandbox/blob/master/hackmd/README.md) | 
[Working Copy](https://hackmd.io/@mhevery/Byaksnk08) ]

## Workflow

### Creating new Document

0. [**One-time-setup**]: Links their HackMD account to the GitHub repository. (Gives the HackMD write rights to the GitHub repo which contains the documents.)
1. Author creates a document in HackMD and creates content as normal.
2. Once ready, author uses the HackMD Version UI to push the document to GitHub.
    - The first time one does this, the author must designate a file in the destination repository. Once that is done the HackMD and GitHub documents are linked. At this point the Author should grab the two URLs and insert them into the document for easier cross-navigation.
    - The "push" from HackMD to GitHub happens whenever the author feels that changes need to be published. The process is to push the "push" button in the HackMD Versions UI.

### Pushing changes to GitHub

Once the documents are linked, any changes from the HackMD can be pushed into GitHub by using the "push" button in the HackMD Version UI. This process is equivalent to pushing a changes to the repo using `git commit; git push`. This process does not have pull-request step. It also implies that the author doing the push must have write permissions to the GitHub repo.

> In practice anyone can edit the HackMD [working copy](https://hackmd.io/@mhevery/Byaksnk08) version of the document per HackMD security settings. The author then decides to accept/reject those changes, and once happy can push them to the GitHub where they would be considered the "truth".

### Discovery and commenting

An important goal of this process would be to allow the community to discover and comment on these documents.

- Because the documents are stored in the GitHub repo, there is a cannon of all documents which are available for the public to read and discover.
- If the reader finds a document of interest and would like to engage in discussion, they would scroll to the top of the document and find the [working copy](https://hackmd.io/@mhevery/Byaksnk08) link. Following that link would bring them to HackMD where they are free to suggest changes, and leave comments or otherwise engage in discussion.
- The author of the document than chooses to accept or reject those changes and to reply to the comments. Once the document is in publishable state the author can than publish the change to GitHub. The author of the document is in control to what is published. This model allows easy way for community to suggest changes, but provides checks to prevent abuse.
    - HackMD recently released new changes to the commenting which allows mentioning of users, hierarchical comments, and comment resolution which greatly improves the usability of HackMD comments.


## GitHub Wiki

Each repository in GitHub comes with [wiki](https://help.github.com/en/github/building-a-strong-community/about-wikis) capability. It would be nice to store our pages on the Wiki. As of right now there does not seem to be a way to linked the Wiki to the HackMD. A request to add support for that has been routed to the HackMD team.

## Limitations

There are some differences about the line endings between GitHub and HackMD. There is a setting for that.

HackMD also has a more powerful markup than what GitHub can process. The implication of that is that some markup may only be visible in HackMD "working copy". (Example would be Math Expressions, or UML diagrams.) The author of the document should consider these limitations when creating the document. 