# Based on [Pure](https://github.com/LeetaoGoooo/pure)

> It's a blog based on github discussion that lets you focus on your creativity. All you need to do is open your browser, log in to github and start your creative journey, no more worry about file, sync deployment and image uploads. What's more  you can migrate your blog in the way you like!

## Dev

Before you do a deployment, you need to config your own `pure.yaml`

```shell
cp pure.sample.yaml pure.yaml
```
Get your own [GITHUB_ACCESS_TOKEN](https://github.com/settings/tokens) here

Then just run the application

```shell
go run main.go
```

### comments

pure use [gitcus](https://github.com/giscus/giscus) as comment system, visit [gitcus-website](https://giscus.app/) to get your repo id ,which can be found in `data-repo-id`

```js
<script src="https://giscus.app/client.js"
    data-repo="[ENTER REPO HERE]"
    data-repo-id="[ENTER REPO ID HERE]"
    data-category="[ENTER CATEGORY NAME HERE]"
    data-category-id="[ENTER CATEGORY ID HERE]"
    data-mapping="pathname"
    data-strict="0"
    data-reactions-enabled="1"
    data-emit-metadata="0"
    data-input-position="bottom"
    data-theme="preferred_color_scheme"
    data-lang="en"
    crossorigin="anonymous"
    async>
</script>
```

## Deploy

Then just run the application

```shell
go build main.go
./main
```
