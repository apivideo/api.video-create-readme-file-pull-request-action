[![badge](https://img.shields.io/twitter/follow/api_video?style=social)](https://twitter.com/intent/follow?screen_name=api_video)
&nbsp; [![badge](https://img.shields.io/github/stars/apivideo/api.video-android-live-stream?style=social)](https://github.com/apivideo/api.video-android-live-stream)
&nbsp; [![badge](https://img.shields.io/discourse/topics?server=https%3A%2F%2Fcommunity.api.video)](https://community.api.video)
![](https://github.com/apivideo/.github/blob/main/assets/apivideo_banner.png)
<h1 align="center">create-readme-file-pull-request-action</h1>

[api.video](https://api.video) is the video infrastructure for product builders. Lightning fast
video APIs for integrating, scaling, and managing on-demand & low latency live streaming features in
your app.

# Table of contents

- [Table of contents](#table-of-contents)
- [Project description](#project-description)
- [Getting started](#getting-started)
  - [Usage](#usage)
- [Documentation](#documentation)
  - [`<documentation_excluded>`](#documentation_excluded)
  - [`<documentation_only>`](#documentation_only)

# Project description

This GitHub action is used in our SDKs repositories to apply some modifications to the README.md file in order to make it more readable on our documentation website.
It then creates a pull request in the given repository with the updated markdown file.

# Getting started

## Usage

```yaml
      - name: Apply changes to the README file
        uses: apivideo/api.video-create-readme-file-pull-request-action@main
        with: 
          source-file-path: "README.md"
          destination-repository: apivideo/api.video-api-client-generator
          destination-path: templates/documentation/sdks/vod
          destination-filename: apivideo-typescript-uploader.md
          pat: "${{ secrets.PAT }}"
```


# Documentation

Here are the tags that can be used in the README.md file to apply some modifications:

## `<documentation_excluded>`

Use this tag to exclude a part of the README.md file from the documentation website.

*Example:*


```markdown
# My title

<!--<documentation_excluded>-->
This part will not be displayed on the documentation website.
<!--</documentation_excluded>-->

blabla
```

## `<documentation_only>`

Use this tag to display a part of the README.md file only on the documentation website.

*Example:*

```markdown
# My title

<!--<documentation_only>
This part will be displayed only on the documentation website.
</documentation_only>-->

blabla
```

