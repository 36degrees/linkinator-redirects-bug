## Steps to reproduce

Run linkinator using `npm run check-links`.

## Expected behaviour

Two broken links should be found:

- /broken, linked from /child-one/grandchild
- /also-broken, linked from /child-two/grandchild

## Actual behaviour

Only the `/broken` link is found.

The only difference is that `/child-one/` is linked to from the root with a trailing slash, and `/child-two` is not.

This means that the `/child-two` link initially 301 redirects to `/child-two/`, though I'm not sure whether the redirection is what's causing the issue.
