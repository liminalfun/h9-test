# House9 Test

Demo link: [house9test.netlify.app](https://house9test.netlify.app)

| Task | Est. Time | Actual Time | Notes |
| ---- | --------- | ----------- | ----- |
|Review brief|0h15m|0h15m||
|Define tools|0h20m|0h15m|Gridsome, Netlify CMS, SCSS (Footnote 1)|
|Initial setup|0h30m|0h45m|(Footnote 2)|
|Add demo content|0h30m|0h40m|(Footnote 3)|
|Base styles|1h00m|2h00m|(Footnote 4)|
|Animation|0h30m|1h00m||
|QA Testing|0h30m|0h30m|All went smoothly!|
|Documentation|0h25|0h25||
|Total|4h00m|5h50m|(Footnote 5)|

## Footnotes

### Footnote 1
“Gridsome is a Vue.js powered Jamstack framework for building static generated websites & apps that are fast by default 🚀.” 

I chose a SSG because I appreciate the speed of both page loading and the development experience. 

Although I’ve never used Gridsome before, I chose it because I’ve been interested in it for a couple weeks. I enjoy working with Vue.js and I recall Max saying in the interview that he also likes to work with Vue.

I decided to go with Netlify CMS rather than hard-coding the content because I want to demonstrate my usual (and ideal) workflow and tooling.

I chose SCSS rather than using a component library or framework (i.e. Bootstrap, Tailwind) because the site’s design is minimal and adding a framework would add unnecessary bulk.|

### Footnote 2
Issue 1:
- Hiccup in github setup because I didn’t create a .gitignore file before running `npm install`. Resolved by (1) delete node_modules, (2) push to main, (3) re-run `npm install`, (3) push to main
- Error message with git-gateway when I logged in. I had run into this issue before, so I just changed the in the config.yml for Netlify CMS to “branch: main” from “branch: master”, and generated a new git-gateway API access token.

### Footnote 3
10 minutes in and starting to add content with the CMS first is causing a kink. So I’m going to just add content directly to the Index.vue file instead, and work on the CMS later if it feels worth it.

### Footnote 4
Ran into an issue with using postcss media queries in Gridsome. Tried troubleshooting and installing different postcss support plugins, but ended up just installing sass instead.

This was my second time using scss mixins, so it took me a bit longer to look through the docs and create my media query strategy.

## Footnote 5
In the end, I ended up not connecting Netlify CMS – as I already surpassed my projected time, and CMS integration was not included in the assignment.

I learned a lot from this challenge!
