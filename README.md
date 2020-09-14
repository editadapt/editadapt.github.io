# HUGO PUBLISH

`Hugo publish` is a Hugo framework to build publishing website: a place where your books AND your website can live together.
It’s using the powerfull ideas behind hugo and uses the theming engine to build some plug-in functionalities.

## Architecture

### Everything is a ~~theme~~ module

Hugo has this amazing thing called the cascade, that allows any user to use theme as building block piece.

if you add this in your Hugo `config.toml`, it will use the element from different theme. Let’s hacve a look at  how this demo site work:

`theme=["pagedjs", "hugo-publish-tufte","hugo-publish-single-column","hugo-publish"]`

1. `pagedjs`: this theme gives us the software and tools to generate PDF (from client side). It’s default part of hugo publish
2. `hugo-publish-tufte`: the theme use for the actual text. It only includes how the content looks like
3. `hugo-publish-single-column`: the theme used to define the website layout (and the reading UX)
4. `hugo-publish`: this create the whole architecture for the website, prepared to handle any new plug-in / theme you may need.

If you want to use the tufte theme, but another layout, change the `hugo-publish-single-column` to whatever you may prefer, and you won’t have to rewrite everything again.

### KINSSBSS (keep it not so stupid but still simple)

- almost no html classes
- simplest HTML first
- not assuming complex layout


# Everything is a publication

