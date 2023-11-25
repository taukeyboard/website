# Tau Keyboard Project Website

## Local Development

Pre-requisites: [Hugo](https://gohugo.io/getting-started/installing/) and [Git](https://git-scm.com)

```shell
# Clone the repo
git clone https://github.com/taukeyboard/website.git

# Change directory
cd website

# Start the server
hugo mod tidy
hugo server --logLevel debug --disableFastRender -p 1313
```

### Add a new blog post
```shell
hugo new content blog/my-first-post.md
```
After finish, remove the `draft: true` from header and push to github.

### Update theme

```shell
hugo mod get -u
hugo mod tidy
```

See [Update modules](https://gohugo.io/hugo-modules/use-modules/#update-modules) for more details.

