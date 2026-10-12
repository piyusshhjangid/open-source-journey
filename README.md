# Open Source Journey

My journey from first-time contributor to independent open-source
contributor. I use this repository to document what I contribute, how I
work through unfamiliar codebases, the feedback I receive, and what I
learn along the way.

## Contributions

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  \#          Project                                                                Issue                                                               PR                                                                  Type             Result
  ----------- ---------------------------------------------------------------------- ------------------------------------------------------------------- ------------------------------------------------------------------- ---------------- -----------
  1           [free-llm-api-hub](https://github.com/pacocartones/free-llm-api-hub)   [#67](https://github.com/pacocartones/free-llm-api-hub/issues/67)   [#198](https://github.com/pacocartones/free-llm-api-hub/pull/198)   Data             Merged
                                                                                                                                                                                                                             verification and 
                                                                                                                                                                                                                             generated        
                                                                                                                                                                                                                             artifacts        

  2           [ChatCops](https://github.com/codercops/chatcops)                      [#94](https://github.com/codercops/chatcops/issues/94)              [#104](https://github.com/codercops/chatcops/pull/104)              TypeScript/DOM   Merged into
                                                                                                                                                                                                                             change, tests,   `dev`
                                                                                                                                                                                                                             changeset        

  3           [ChatCops](https://github.com/codercops/chatcops)                      [#92](https://github.com/codercops/chatcops/issues/92)              [#120](https://github.com/codercops/chatcops/pull/120)              Inline widget    Merged /
                                                                                                                                                                                                                             visibility and   issue
                                                                                                                                                                                                                             accessibility    closed
                                                                                                                                                                                                                             fix              
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Latest Milestone

My third contribution addressed an inline ChatCops panel that remained
in the keyboard focus order after `close()` was called. I removed CSS
overrides that bypassed the `cc-visible` state and added
`visibility: hidden` for the closed inline state. The maintainer
verified the behavior and issue #92 was closed as completed via PR #120.

Validation included a successful workspace build, 190 passing tests
across 26 test files, type checking, Git whitespace checks, and manual
open/close/reopen verification. I also supplied screenshots of the open
and closed states and disclosed how I used AI assistance.

See the full record: [Contribution #3 --- ChatCops
#92](contributions/003-chatcops-92.md).

## Current Focus

-   Independent implementation and debugging in unfamiliar codebases
-   Writing and understanding unit tests, not only running them
-   Git/GitHub workflow and responding to code review
-   CI/CD, build checks, and type checking
-   Understanding source-of-truth files and generated artifacts
-   Communicating clearly with maintainers
-   Building a consistent contribution record while preparing for GSoC
    2027

## Goals

-   Make meaningful open-source contributions
-   Become comfortable working in unfamiliar codebases
-   Improve testing and debugging skills through real code changes
-   Participate in SWoC, where suitable
-   Prepare for GSoC 2027 while remembering that 2027 participation
    depends on the official accepted-organization list

## Contribution Journal

Detailed contribution records are stored in the `contributions/`
directory.

-   [Contribution #1 --- free-llm-api-hub
    #67](contributions/001-free-llm-api-hub-67.md)
-   [Contribution #2 --- ChatCops #94](contributions/002-chatcops-94.md)
-   [Contribution #3 --- ChatCops #92](contributions/003-chatcops-92.md)
