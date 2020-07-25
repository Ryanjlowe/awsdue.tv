# AWS DUE TV

AWS DUE Video Collection

## Developer guide

This workshop is built with markdown as a static HTML site using [Hugo](http://gohugo.io) and the [Learn theme for Hugo](https://learn.netlify.com/en/).

#### Clone this repo

The theme is referenced as a [git-submodule](https://git-scm.com/docs/git-submodule).

`git clone --recurse-submodules git@github.com:Ryanjlowe/awsdue.tv.git`

#### Install and run Hugo

##### Homebrew (macOS)

If you are on macOS and using [Homebrew](https://brew.sh/), you can install Hugo with the following one-liner:

`brew install hugo`

For other platforms, please see Hugo's [Getting Started](https://gohugo.io/getting-started/installing/) docs.

#### Run Hugo locally

`hugo serve -D`

Visit http://localhost:1313/ to see the site.

#### Create and edit content

The easiest way to add content is with the `hugo new` command. You can create new content files in Hugo using the `hugo new` command. By default, Hugo will create new content files with at least date, title (inferred from the file name), and `draft = true`. This saves time and promotes consistency for sites using multiple content types. You can create your own [archetypes](https://gohugo.io/content-management/archetypes/) with custom preconfigured front matter fields as well.

`hugo new a-chapter/my-page-title.md`

The newly created content file will show up under the `/content/` directory. In the example above, the file would be `/content/a-chapter/my-page-title.md`.

As you save edits to a page, the site will live-reload to show your changes.

Note: shift-reload may be necessary in your browser to reflect the latest changes.

## License Summary

Copyright 2019 Amazon.com, Inc. or its affiliates. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License").
You may not use this file except in compliance with the License.
A copy of the License is located at

    http://www.apache.org/licenses/LICENSE-2.0

or in the "license" file accompanying this file. This file is distributed
on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either
express or implied. See the License for the specific language governing
permissions and limitations under the License.
