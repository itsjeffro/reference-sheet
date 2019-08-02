# Subqueries

Helpful snippets to reference.

## Joins

### Get highest record

Tables examples

* Posts
* Revisions

```sql
SELECT *

FROM posts

INNER JOIN (
    SELECT 
        id AS revision_id,
        max(created_at) AS recent,
        post_id
    
    FROM revisions
    
    GROUP BY post_id
) AS rv ON rv.task_id = posts.id;
```
