Nomenclature
============

How to name things?


### External data source

#### Access
- `fetch` Read: file, object from database
- `store` Write: file, object to database


### Object

#### Construct unique(ish)
Not (easily) reproducible, such as UUIDs, random sequences.
- `new`

#### Construct mutable
- `create`

### Construct immutable
- `cons`

### Access
- `get_[..]`
- `set_[..]`


### Collection

#### Construct mutable
- `create`

### Construct immutable
- `empty`

#### Access K/V (including indexed)
- `get`
- `set`

#### Access set
- `add`
- `remove`
- `is_member`
- `union`
- `diff`

#### Access queue (FIFO)
Which pair is better?

| Pair                 | Pros                         | Cons |
|----------------------|------------------------------|------|
| `enqueue`, `dequeue` | explicit, suggest fair order | long |
| `in`, `out`          | short, intuitive, same words as in order spec acronym | _may_ also mean out of order manipulations |
| `add`, `remove`      | intuitive, consistent with set accessors | a bit longer than in/out |

#### Access stack (LIFO)
- `push`
- `pop`

Why differentiate between LIFO and FIFO accessors? The should ideally be uniform.

### Traverse sequence
- `iter`
- `map`
- `filter`
- `fold`
