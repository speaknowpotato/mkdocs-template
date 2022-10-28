---
comments: true
tags:
    - how-to
---

# Adding a comment system


1.  __Install the [Giscus GitHub App]__ and grant access to the repository that should host comments as GitHub discussions. Note that this can be a repository different from your documentation.
2.  __Visit [Giscus] and generate the snippet__ through their configuration tool to load the comment system. Copy the snippet for the next step. The resulting snippet should look similar to this:

    ```html
    <script src="https://giscus.app/client.js"
            data-repo="speaknowpotato/mkdocs-template"
            data-repo-id="R_kgDOIPlEiw"
            data-category="General"
            data-category-id="DIC_kwDOIPlEi84CSPcD"
            data-mapping="pathname"
            data-strict="0"
            data-reactions-enabled="1"
            data-emit-metadata="0"
            data-input-position="top"
            data-theme="preferred_color_scheme"
            data-lang="en"
            crossorigin="anonymous"
            async>
    </script>
    ```
3. __Add theme extension and override the [`comments.html`][comments]__. More details could be found in [Setup and theme structure](https://squidfunk.github.io/mkdocs-material/customization/#setup-and-theme-structure). 
   
    1. Create a new folder `overrides` in the relative folder. [Example](https://github.com/speaknowpotato/mkdocs-template/tree/main/overrides/partials)
    
    2. Change `theme/custom_dir` to `overrides` in `mkdocs.yml` [Example](https://github.com/speaknowpotato/mkdocs-template/blob/main/mkdocs.yml)
    
    3. Update `comments.html` [Example](https://github.com/speaknowpotato/mkdocs-template/blob/main/overrides/partials/comments.html)
  
4. __Enable comment__, add the following lines to each markdown file that you want to have comment system. 
   ```
   ---
   comments: true
   ---
   ```

## Reference
1. [Adding a comment system](https://squidfunk.github.io/mkdocs-material/setup/adding-a-comment-system/)






  [Giscus GitHub App]: https://github.com/apps/giscus
  [Giscus]: https://giscus.app/
  [comments]: https://github.com/squidfunk/mkdocs-material/blob/master/src/partials/comments.html

