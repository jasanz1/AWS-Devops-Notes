Git is a [free and open source](https://git-scm.com/about/free-and-open-source) distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Git is [easy to learn](https://git-scm.com/doc) and has a [tiny footprint with lightning fast performance](https://git-scm.com/about/small-and-fast). It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like [cheap local branching](https://git-scm.com/about/branching-and-merging), convenient [staging areas](https://git-scm.com/about/staging-area), and [multiple workflows](https://git-scm.com/about/distributed).

### Characteristics

##### Strong Support for Non-linear Development

Git supports rapid branching and merging, and includes specific tools for visualizing and navigating a non-linear development history. In Git, a core assumption is that a change will be merged more often than it is written, as it is passed around to various reviewers. In Git, branches are very lightweight: a branch is only a reference to one commit. With its parental commits, the full branch structure can be constructed.[improper synthesis?](https://en.wikipedia.org/wiki/Wikipedia:No_original_research#Synthesis_of_published_material "Wikipedia:No original research")_

##### Distributed Development

Like [Darcs](https://en.wikipedia.org/wiki/Darcs "Darcs"), [BitKeeper](https://en.wikipedia.org/wiki/BitKeeper "BitKeeper"), [Mercurial](https://en.wikipedia.org/wiki/Mercurial "Mercurial"), [Bazaar](https://en.wikipedia.org/wiki/Bazaar_(software) "Bazaar (software)"), and [Monotone](https://en.wikipedia.org/wiki/Monotone_(software) "Monotone (software)"), Git gives each developer a local copy of the full development history, and changes are copied from one such repository to another. These changes are imported as added development branches and can be merged in the same way as a locally developed branch.[43](https://en.wikipedia.org/wiki/Git#cite_note-44)

##### Compatibility with Existing Systems and Protocols

Repositories can be published via [Hypertext Transfer Protocol Secure](https://en.wikipedia.org/wiki/HTTPS "HTTPS") (HTTPS), [Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol "Hypertext Transfer Protocol") (HTTP), [File Transfer Protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol "File Transfer Protocol") (FTP), or a Git protocol over either a plain socket or [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell "Secure Shell") (ssh). Git also has a CVS server emulation, which enables the use of existing CVS clients and IDE plugins to access Git repositories. [Subversion](https://en.wikipedia.org/wiki/Apache_Subversion "Apache Subversion") repositories can be used directly with git-svn.[44](https://en.wikipedia.org/wiki/Git#cite_note-45)

###### Efficient Handling of Large Projects

Torvalds has described Git as being very fast and scalable,[45](https://en.wikipedia.org/wiki/Git#cite_note-46) and performance tests done by Mozilla[46](https://en.wikipedia.org/wiki/Git#cite_note-47) showed that it was an [order of magnitude](https://en.wikipedia.org/wiki/Order_of_magnitude "Order of magnitude") faster diffing large repositories than [Mercurial](https://en.wikipedia.org/wiki/Mercurial "Mercurial") and [GNU Bazaar](https://en.wikipedia.org/wiki/GNU_Bazaar "GNU Bazaar"); fetching version history from a locally stored repository can be one hundred times faster than fetching it from the remote server.[47](https://en.wikipedia.org/wiki/Git#cite_note-48)

##### Cryptographic Authentication of History

The Git history is stored in such a way that the ID of a particular version (a _commit_ in Git terms) depends upon the complete development history leading up to that commit. Once it is published, it is not possible to change the old versions without it being noticed. The structure is similar to a [Merkle tree](https://en.wikipedia.org/wiki/Merkle_tree "Merkle tree"), but with added data at the nodes and leaves.[48](https://en.wikipedia.org/wiki/Git#cite_note-49) ([Mercurial](https://en.wikipedia.org/wiki/Mercurial "Mercurial") and [Monotone](https://en.wikipedia.org/wiki/Monotone_(software) "Monotone (software)") also have this property.)

##### Toolkit-based Design

Git was designed as a set of programs written in [C](https://en.wikipedia.org/wiki/C_(programming_language) "C (programming language)") and several shell scripts that provide wrappers around those programs.[49](https://en.wikipedia.org/wiki/Git#cite_note-50) Although most of those scripts have since been rewritten in C for speed and portability, the design remains, and it is easy to chain the components together.[50](https://en.wikipedia.org/wiki/Git#cite_note-51)

##### Pluggable Merge Strategies

As part of its toolkit design, Git has a well-defined model of an incomplete merge, and it has multiple algorithms for completing it, culminating in telling the user that it is unable to complete the merge automatically and that manual editing is needed.[51](https://en.wikipedia.org/wiki/Git#cite_note-52)

##### [Garbage](https://en.wikipedia.org/wiki/Garbage_(computer_science) "Garbage (computer science)") Accumulates until Collected

Aborting operations or backing out changes will leave useless dangling objects in the database. These are generally a small fraction of the continuously growing history of wanted objects. Git will automatically perform [garbage collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science) "Garbage collection (computer science)") when enough loose objects have been created in the repository. Garbage collection can be called explicitly using `git gc`.[52](https://en.wikipedia.org/wiki/Git#cite_note-53)

##### Periodic Explicit Object Packing

Git stores each newly created object as a separate file. Although individually compressed, this takes up a great deal of space and is inefficient. This is solved by the use of _packs_ that store a large number of objects [delta-compressed](https://en.wikipedia.org/wiki/Delta_encoding "Delta encoding") among themselves in one file (or network byte stream) called a _packfile_. Packs are compressed using the [heuristic](https://en.wikipedia.org/wiki/Heuristic_(computer_science) "Heuristic (computer science)") that files with the same name are probably similar, without depending on this for correctness. A corresponding index file is created for each packfile, telling the offset of each object in the packfile. Newly created objects (with newly added history) are still stored as single objects, and periodic repacking is needed to maintain space efficiency. The process of packing the repository can be very computationally costly. By allowing objects to exist in the repository in a loose but quickly generated format, Git allows the costly pack operation to be deferred until later, when time matters less, e.g., the end of a workday. Git does periodic repacking automatically, but manual repacking is also possible with the `git gc` command. For data integrity, both the packfile and its index have an [SHA-1](https://en.wikipedia.org/wiki/SHA-1 "SHA-1") checksum inside, and the file name of the packfile also contains an SHA-1 checksum. To check the integrity of a repository, run the `git fsck` command.[53](https://en.wikipedia.org/wiki/Git#cite_note-Git_-_Packfiles-54)
