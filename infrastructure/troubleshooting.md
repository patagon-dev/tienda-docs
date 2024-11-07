---
title: troubleshooting
description: 
published: true
date: 2024-11-07T19:28:37.594Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:12:54.617Z
---

# Troubleshooting

## Create Admin user


> Assign the **admin** role to a user using the user RUT value
{.is-info}

Log into the rails console:

```ruby
docker compose run web rails c
```

Search for the user. If RUT is 44.444.444-4, use `444444444`:

```ruby
u = Spree::User.find_by(run: '444444444')
```

The search for the **admin** role and assign the role to the user:

```ruby
role = Spree::Role.find_by(name: 'admin')
u.spree_roles << role
u.save
```

