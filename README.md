# Gatsby Remark Fountain extension

Adds [Fountain](https://fountain.io) code support to Gatsby's Remark integration.


## Example

When installed, this will turn:

```markdown
    This is a bit of dialogue from the movie:

    ```fountain
    INT. NCIS OFFICE - DAY

    GIBBS
    Records of the cab company?
    
    ZIVA
    Working on it.
    ```
```

Into this:

```html
    <p>This is a bit of dialogue from the movie:</p>

    <div class="fountain-body fountain-body-inline">
        <h3>INT. NCIS OFFICE - DAY</h3>
        <div class="dialogue">
            <h4>GIBBS</h4>
            <p>Records of the cab company?</p>
        </div>
        <div class="dialogue">
            <h4>ZIVA</h4>
            <p>Working on it.</p>
        </div>
    </div>
```


## Installation

```shell
yarn add gatsby-remark-fountain
```

Then, add it to the configuration of the `gatsby-transformer-remark`
plugin in your `gatsby-config.js` file:

```js
{
  resolve: "gatsby-transformer-remark", 
  options: {
    plugins: [
      "gatsby-remark-fountain"
    ]
  }
}
  ```

If you also use `gatsby-remark-prismjs` or a similar syntax highlighter, make sure to include it after the `gatsby-remark-fountain` plugin. Order matters!
