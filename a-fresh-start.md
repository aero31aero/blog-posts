# A Fresh Start

So... This is my blog. What makes it special is what I'll be bragging about now.

## First blog powered by Raia

First things first, what is Raia? Well, it is the only (that I know of) single page static site blog engine. Jekyll and the others were not single page, and I wanted to give the single page format a try, so I ended up writing my own. The journey was worth it and I believe I've on my hands a very compact and fast blog engine. Here are some stats that you might like:

1. Raia core loads in less than 70kB and makes only 3 HTTP requests at the time of writing.
2. Total page load, after uncompressing, takes 185 kB.

So, even though I have put a simple loading animation, hopefully you would not get much time to look at it.

## Optimizations

There is a simple idea behind Raia- when loading another post, why fetch and render the complete page again? Even if your browser is smart enough to cache all the resources, there is still the matter of rendering the pages again. Also, a reload breaks the visual continuity on slow connections.

With that in mind, Raia only fetches the markdown content of the post to be rendered, which takes only as much as the size of the post's text, and nothing more. This means that after an initial load of approzimately 200kB (uncompressed), the consecutive posts load at around a few kBs each. Neat, right?

The initial file size of 70kB was itself an interesting challenge to reach. Right now, I have set up a `gulp` task to concatenate and compress all the stylesheets and scripts into their own files, as well as replace references to them and compress the `html` file. On top of that, GitHub's servers enable `gzip2` compression on compatible browsers, resulting in this figure.

## Development

Currently, I plan to add support for Disqus comments and add proper error handling messages. Also, the mobile support is pretty much nil right now and needs some work to get it right. There is a list of other minor issues I have to resolve, including an easy deployment method. Once that is done, the project should be mature enough to not require frequent commits anymore and be usable.

The one problem that I can't quite figure out is SEO. A single page website renders itself badly when a search engine's spider comes crawling by, and usually sites circumvent that by providing a stati version of their site to the robots. However, that would mean I would have to implement a static site *generator* that I tried not to do with this whole project. Even then, it would need to be properly mapped to the correct post urls in the single page app.

## Conclusion

Well, it feels nice to have worked on something and see it in action, functioning just like you imagined it would. The eternal question of *should I roll out my own blog* had been troubling me for quite a while whnen I failed to find anything that suited my tastes, so I don't have any qualms (**yet**) about my decision to reinvent the wheel, mainly because this particular wheel is structurally different from others, and because it was fun.

If you are geeky enough, you might want to take a look at the [source code](https://github.com/aero31aero/raia) on GitHub. The developer environment is hosted [here](http://rohitt.me/raia/dist) and you'd find multiple sample posts there. Till I add comments, leave me some feedback in some other manner. Thanks for reading. :D
