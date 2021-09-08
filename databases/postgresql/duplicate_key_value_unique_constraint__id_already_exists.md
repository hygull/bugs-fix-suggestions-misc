## Issue

```python
`duplicate key value violates unique constraint "users_classificationcompletion_pkey"
DETAIL:  Key (id)=(67) already exists`

```

## Generator Action

- Creating an instance from Django Admin Interface
- Creating an instance from Django Interactive shell

## Links (Stackoverflow)

1. [postgresql duplicate key violates unique constraint](https://stackoverflow.com/a/59113705/6615163)

2. [How to reset the sequence for IDs on PostgreSQL tables](https://stackoverflow.com/a/14589706/6615163)

## Fix 

> I used 1st one to solve

`python manage.py sqlsequencereset | python manage.py dbshell`
