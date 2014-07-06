The xTuple Server calculates the ideal Postgres configuration values for your machine. It carefully discerns, based on system resources and environment, the following values in `postgresql.conf`:

- `work_mem`
- `shared_buffers`
- `effective_cache_size`
- `max_stack_depth`

It also automatically configures your kernel via `sysctl` to accommodate an enlarged `shared_buffers`, and configures the [Postgres Genetic Query Optimizer](http://www.postgresql.org/docs/9.3/static/geqo.html).