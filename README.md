# real-links-blog

Engineering blog for Real Links

Built using [Jekyll](https://jekyllrb.com).

## Development

Quickest way to get started is using Docker & the [jekyll/minimal](https://hub.docker.com/r/jekyll/minimal) image:

```
docker run --rm -v $PWD:/srv/jekyll -p 4000:4000 -it jekyll/minimal jekyll serve
```

## Writing Posts

Following [the Jekyll pattern](https://jekyllrb.com/docs/posts/), write posts as HTML or Markdown files in [`_posts`](_posts/) & push to `master` to deploy it. You can embed content, such as images, HTML markup & included blocks.

### Included Blocks

There are a handful of "blocks" that you can include on the page, and pass parameters to for configuration.

#### Callout

Based on [Notion's callout blocks](https://www.notion.so/Callout-blocks-5b2638247b54447eb2e21145f97194b0), this block is useful for highlighting specific text or breaking out from the rest of the page:

```html
{% include callout.html
    emoji="👋"
    text="Hello world!"%}
```

![Single-line embed block](/img/readme/callout-1.png)

#### Embed

Based on [Notion's embed blocks](https://www.notion.so/Embeds-6b7133323590447b9d8e963c136ebce5) or [Embedly Cards](https://embed.ly/cards), this block is useful for embedding nice-looking links into the page as blocks. In it's simplest form:

```html
{% include embed.html url="https://reallinks.dev"%}
```

[![Single-line embed block](/img/readme/embed-1.png)](https://reallinks.dev)

However, there are additional properties you can add to decorate the embed. As of now this must be done by hand, but the results still look good:

```html
{% include embed.html
    emoji="🚀"
    title="Real Links"
    description="Rocket-fuel your employee referral hires"
    url="https://www.reallinks.io"
    image="/img/2020-02-15-hello-world-2.png"%}
```

[![Multiple-line embed block](/img/readme/embed-2.png)](https://reallinks.io)

## To-Do

- [ ] Nicer embed blocks for specific types of content, e.g. video

- [ ] Once Notion release an API, move the content over to Notion & get the pages to render content directly from Notion. Either continuing with Jekyll or moving to a Vue project, where the entire site is pre-rendered.
