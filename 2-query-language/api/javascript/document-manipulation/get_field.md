---
layout: api-command 
language: JavaScript
permalink: api/javascript/get_field/
command: ()
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/javascript/document-manipulation/get_field.md
io:
    -   - sequence
        - sequence
    -   - singleSelection
        - value
    -   - object
        - value
related_commands:
    row: row/
---

{% apibody %}
sequence(attr) &rarr; sequence
singleSelection(attr) &rarr; value
object(attr) &rarr; value
{% endapibody %}

Get a single field from an object. If called on a sequence, gets that field from every
object in the sequence, skipping objects that lack it.

__Example:__ What was Iron Man's first appearance in a comic?

```js
r.table('marvel').get('IronMan')('firstAppearance').run(conn, callback)
```

