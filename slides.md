---
theme: default
background: https://res.cloudinary.com/practicaldev/image/fetch/s--VwKuRA_r--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/427yh9kull5oycojetde.png
class: 'text-center'
highlighter: prism
lineNumbers: false
info: |
  ## Deep Dive into Git.
drawings:
  persist: false
css: unocss
---

# Deep Dive into Git 

<div class="absolute top-1 right-4 pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/raminjafary" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# Agenda

- Version control using Git
- Bitkeeper, SourcePuller, and the birth of Git
- Git
- Git vs Mercurial
- Git vs SVN (Subversion)


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# What is version control or SCM?

  - Also known as revision control, source control, or source code management 
  - Tracking and managing changes to software code. 
  - Version control systems are software tools that help software teams manage changes to source code over time. 
  - Changes are usually identified by a number or letter code, termed the "revision number", "revision level", or simply "revision". 
  - Each revision is associated with a timestamp and the person making the change. 
  - Revisions can be compared, restored, and, with some types of files, merged.
  - Source code management (SCM) is used to track modifications to a source code repository. 
  - SCM tracks a running history of changes to a code base and helps resolve conflicts when merging updates from multiple contributors. 
  - SCM is also synonymous with Version control. 

---
layout: default
---

# Bitkeeper and SourcePuller

  - Bitkeeper developed as proprietary software by BitMover Inc. (CEO Larry McVoy, who was also a Linux contributor)
  - As a solution to some of the growing pains that Linux was having in September 1998.
  - Early access betas were available in May 1999 and on May 4, 2000, 
  - The first public release of BitKeeper was made available.
  - Some, including GNU Project founder Richard Stallman and including Linux veteran Alan Cox, expressed concern about proprietary tools being used on a flagship free project. 
  - BitMover added gateways which allowed limited interoperation between the Linux BitKeeper servers (maintained by BitMover) and developers using CVS and Subversion. 
  - Andrew Tridgell reverse engineered the BitKeeper protocol. SourcePuller was born as an open-source client for accessing the BitKeeper version control system.
  - SourcePuller sparked the switch of the Linux kernel from BitKeeper to Git
  - Bitkeeper was released as open-source software under the Apache-2.0 license on 9 May 2016.
  - BitKeeper is no longer being developed:(


[^1]: [Learn More](https://sli.dev/guide/syntax.html#line-highlighting)

---

# Git

  - Git is free and open source software for distributed version control distributed under the GPL-2.0-only license.
  - Its goals include speed, data integrity, and support for distributed, non-linear workflows (thousands of parallel branches running on different systems)
  - Authored by Linus Torvalds in 2005 for development of the Linux kernel
  - unlike most client–server systems, every Git directory on every computer is a full-fledged repository with complete history and full version-tracking abilities, independent of network access or a central server.
  - The development of Git began on 3 April 2005.
  - Torvalds announced the project on 6 April and became self-hosting the next day.
  - The first merge of multiple branches took place on 18 April.
  - On 16 June, Git managed the kernel 2.6.12 release.
  - Torvalds turned over maintenance on 26 July 2005 to Junio Hamano, a major contributor to the project.
  - Since 2005, Junio Hamano has been the core maintainer.
  - Torvalds sarcastically quipped about the name git (which means "unpleasant person" in British English slang).
  - The man page describes Git as "the stupid content tracker". The read-me file of the source code elaborates further:[27]

---
class: px-20
---
# Git vs Mercurial

Both version control systems, i.e., Mercurial and Git are distributed version control systems (DVCS).

<div class="flex">
  <div grid="~ cols-1 gap-4" m="-t-2">

  - Git is a little bit of complex than Mercurial.	
  - A branch is a pointer to a commit (SHA).
  - Mutable through rollback, cherry-pick, rebase	
  - Each revision unique by calculated SHA-1
  - Supported via revert command; arbitrary via rebase and cherry-pick.
  - Git supports the staging area, which is known as the index file.	

  </div>

  <div grid="~ cols-1 gap-4" m="-t-2">

  - Git is a little bit of complex than Mercurial.
  - A branch is embedded in a commit; branches cannot be renamed or deleted.
  - Immutable beyond rollback.
  - Incremental, numerical index of revision (0, 1, 2, etc).
  - Supported via backout, revert commands
  - There is no index or staging area before the commit in Mercurial.

  </div>
</div>

---
preload: false
---

# Git vs SVN


<div class="flex">
  <div grid="~ cols-1 gap-4" m="-t-2">

  - It's a distributed version control system
  - Git is an SCM (source control is specific to source code, also covers large binary files and digital assets).
  - Git has a cloned repository.
  - The Git branches are familiar to work. The Git system helps in merging the files quickly and also assist in finding the unmerged ones.	
  - Git does not have a Global revision number.	  
  - Git has cryptographically hashed contents that protect the contents from repository corruption taking place due to network issues or disk failures.	
  - Git stored content as metadata.	

  </div>

  <div grid="~ cols-1 gap-4" m="-t-2">

  - It's a Centralized version control system
  - SVN is revision control. (digitial)
  - SVN does not have a cloned repository.
  - The SVN branches are a folder which exists in the repository. Some special commands are required For merging the branches.
  - SVN has a Global revision number.
  - SVN does not have any cryptographically hashed contents.
  - SVN stores content as files.
  - SVN's content is less secure than Git.
  </div>
</div>

---
layout: center
class: text-center
---

# Thank you
##### Ramin Jafary