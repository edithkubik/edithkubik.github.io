# phischolz.github.io

## Picture options

Pictures on **Home** (projects), **News** and **Outreach** can each be adjusted.
Add any of these lines directly under the picture's `image:` line, in
`_data/projects.yml`, `_data/outreach.yml`, or at the top of a news post in `_posts/`.
All of them are optional.

| Setting | Values | What it does |
|---|---|---|
| `image_fit` | `contain` (default) | Shows the whole picture; may leave empty space around it |
| | `cover` | Fills the whole frame; the edges get cropped |
| `image_focus` | `center` (default), `top`, `bottom`, `left`, `right`, `top left`, ... | With `cover`: which part of the picture to keep |
| `image_scale` | `1` (default), `0.9`, `0.8`, ... | Shrinks the picture inside its frame, leaving a border. `0.8` = 80% (`80%` also works) |

Example:

```yaml
- title: Research Ireland Pathway Fellowship
  description: ...
  image: /assets/images/REg.png
  image_scale: 0.8
```

On **Outreach**, pictures already keep their natural shape, so only `image_scale` makes a visible difference there.
People photos on the People page are not affected.

**Watch out for colons:** if any text contains a colon followed by a space
(for example `Image credit: NASA`), put the whole text in double quotes,
otherwise the site fails to build and the live page stops updating.
