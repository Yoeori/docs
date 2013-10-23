---
layout: api-command 
language: Ruby
permalink: api/ruby/db_list/
command: db_list
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/ruby/accessing-rql/db_list.md
related_commands:
    db_create: db_create/
    db_drop: db_drop/
---


{% apibody %}
r.db_list() &rarr; array
{% endapibody %}

List all database names in the system. The result is a list of strings.

__Example:__ List all databases.

```rb
r.db_list.run(conn)
```