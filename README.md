# migrid-benchmark (WIP)

A collection of tools for benchmarking the performance of I/O services in migrid deployments.


## Work In Progress

The collection is currently being built with the intention of providing coverage of most of the I/O services in the MiGrid deployments.
The tool is currently being built with ERDA as its target, but the goal is to make the tools deployment-agnostic so that it works for all MiGrid deployments.

The initial goal is to create a bench tool which, when called, will utilize a CLI tool to produce some tables that outputs numbers indicating the performance and potentially provide information regarding bottlenecks or unseen issues.
Here, [Hyperfine](https://github.com/sharkdp/hyperfine) might be worth looking into.

In order to make the tool work with ERDA, we use [Puppeteer](https://pptr.dev/) to log in and navigate through the pages.

The initial goal is to make a benchmarking tool which can produce information on the following I/O services in ERDA:
- Share links
- Network Drives
- Rclone
- Duplicity
- FileZilla/SFTP

Currently, the following TODO is as follows:
- [] Login to ERDA via the bench tool by providing a link, username and password.
  - We need to make a test account and/or make authorization work with this login too
- [] It should navigate to Share Links
  - We should make a small example run of it, and decide on how to benchmark it the most effectively

After this work is done, it should be looked into what strengths and weaknesses is observable, and then build upon it to provide support for the remainder of the I/O services.
