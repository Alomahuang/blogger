---
title: Query record with newlines
date: 2022-11-18 T00:00:00-00:00
categories:
  - Web
tags:
  - Ruby on Rails
  - ActiveRecord
  - PostgreSQL
toc: true
toc_sticky: true
---

I have to remove the newlines character if the column has any, but with '%/r/n%,' I can't locate any record, and here's how to solve the problem.
{: .notice--info}

## SQL

I am using PostgreSQL and rails in this case.
In SQL record, I can see the result, including the content like 'example /r/n example,' but whenever I use the query

```sql
select *
from table
where column like '%/r/n%'
```
I will have no result.

turns out

I do not need to put escape here, I need to un-escape it, according to this amazing [stackflow post](https://stackoverflow.com/questions/67421846/postgres-how-to-find-text-that-contains-a-newline-character-using-like)
and basically, I just need to change the query to

```sql
select *
from table
where column like E'%\n%'
```

or literally(which is so cool), put a newlines in the query like
```sql
select *
from table
where column like '%
%'
```
And you will get the result records!

## ActiveRecord
For ruby on rails with ActiveRecord interface i use:
```ruby
Table.where('column like ?','%
%')
```
And it will return the proper record.

I hope this helps you as it helps me a lot!

Happy coding!










