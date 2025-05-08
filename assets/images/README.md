# Images for Protocol Primer

This directory contains images used in Protocol Primer articles and pages.

## Directory Structure

- `assets/images/` - Main images directory
  - `posts/` - Images for blog posts, organized by post name
  - `pages/` - Images for static pages
  - `common/` - Shared images used across the site

## How to Add Images to Your Articles

### 1. Add the image file to the appropriate directory

For blog posts, create a subdirectory in `assets/images/posts/` with a name that matches your post:

```
assets/images/posts/post-name/image1.jpg
assets/images/posts/post-name/image2.png
```

For pages, add images to the `assets/images/pages/` directory:

```
assets/images/pages/about/team.jpg
```

### 2. Reference the image in your Markdown

To add an image to your article, use the following Markdown syntax:

```markdown
![Alt text description](/protocolprimer/assets/images/posts/post-name/image1.jpg)
```

Or with custom styling:

```markdown
<img src="/protocolprimer/assets/images/posts/post-name/image1.jpg" alt="Description" width="500" class="align-center">
```

### 3. Image Alignment

You can align images using the following classes:

- `align-left` - Left alignment
- `align-center` - Center alignment
- `align-right` - Right alignment

Example:

```markdown
<img src="/protocolprimer/assets/images/posts/post-name/image1.jpg" alt="Description" class="align-right">
```

### 4. Image Figure with Caption

To add a caption to your image, use the figure element:

```markdown
<figure>
  <img src="/protocolprimer/assets/images/posts/post-name/image1.jpg" alt="Description">
  <figcaption>This is a caption for the image.</figcaption>
</figure>
``` 