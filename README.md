# Amazon Pinpoint Workshop

AWS Workshop tutorial to learn how to engage with your customers by using Amazon Pinpoint.

## Developer guide

This workshop is built with markdown as a static HTML site using [Hugo](http://gohugo.io).

#### Install Hugo

On a mac:

`brew install hugo`

On Linux:
  - Download from the releases page: https://github.com/gohugoio/hugo/releases
  - Extract and save the executable to `/usr/local/bin`

#### Clone this repo

`git clone git@github.com:aws-samples/amazon-pinpoint-workshop.git`

#### Clone the theme submodule:

This repository uses the [Learn theme for Hugo](https://learn.netlify.com/en/). The theme is referenced as a [git-submodule](https://git-scm.com/docs/git-submodule).

```sh
cd amazon-pinpoint-workshop
git submodule init
git submodule update --checkout --recursive
```

#### Install node packages:

`npm install`

#### Run Hugo locally:

`npm run server`
or
`npm run test` to see stubbed in draft pages.

or 

`hugo serve -D`

#### View Hugo locally

Visit http://localhost:1313/ to see the site.

#### Making Edits

As you save edits to a page, the site will live-reload to show your changes.

note: shift-reload may be necessary in your browser to reflect the latest changes.

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
