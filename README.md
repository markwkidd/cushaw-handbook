# Commonwealth Cushaw Project documentation repository

This git repository contains all of the content as well as the Jeckyll scripts that are used to generate the website for the Commonwealth Cushaw Project.

## Using images

Images should be stored in `/assets/images`, within a subfolder that corresponds to the subfolder name of the 'primary' page that uses the image. An image related to a Cushaw Pumpkin Pie recipe should be stored at the path `/assets/images/recipes/cushaw-pumpkin-pie`.

### Image without caption
Without a caption, an image can be embedded using Markdown syntax, for example:
```
![Drying seeds in a colander just removed from cushaw fruit]( {{ '/assets/images/recipes/cut-fruit-with-seeds-350w.jpg' | relative_url }} )
```

### Image with caption
Invoke the template to incorporate an image with a caption using the html element `figcaption`.
```
{% include caption-image.html src="/assets/images/recipes/cut-fruit-with-seeds-350w.jpg" alt="Saved seeds in a colander" caption="Seed saving and sharing is integrated into the guide" %}
```

## Wrapping text via floating images
Add `{:class="float-right-third"}` after either a captioned or non-captioned image in order to set it to float to one-third the width of the browser window. _Note: mobile devices and other small screens will see each image at the full width instead of one-third width._ Up to three images can be floated in a line using this tag.

Example of wrapping text around floating non-captioned image:
```
![Drying seeds in a colander just removed from cushaw fruit]( {{ '/assets/images/recipes/cut-fruit-with-seeds-350w.jpg' | relative_url }} )
{:class="float-right-third"}
```

Example of wrapping text around floating captioned image:
```
{% include caption-image.html src="/assets/images/recipes/cut-fruit-with-seeds-350w.jpg" alt="Saved seeds in a colander" caption="Seed saving and sharing is integrated into the guide" %}
{:class="float-right-third"}
```