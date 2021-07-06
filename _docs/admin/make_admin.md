---
layout: default
title: Grant/revoke admin privileges
parent: Administration
nav_order: 2
has_children: false
last_modified_date: 2021-07-04 11:21
---

# Grant/revoke admin privileges

**Attention:** Administrator privileges confer rights to users to perform administrative actions, such as removing users and resources. Such actions are to be used with great care and after a careful and considered decision process!

**Technical prerequisites:** Access to the `rails` console (and knowledge of how to use basic Ruby).

## Granting admin privileges

From a terminal, access a `rails console` session. If you are accessing a machine using `ssh` or have a local session, simply type `rails console` or `bundle exec rails console` while in the directory where cyhoeddwn has been installed. If you are using Heroku, change directory on your local machine to where you have deployed cyhoeddwn and launch the console using `heroku run rails console` or `heroku run bundle exec rails console`, this may take a little while to load.

In either case you will be presented with an interactive Ruby (`irb`) prompt.

![](/assets/img/admin/irb.png)

You'll need to find the user from Active Record, to do this, set a variable (say `user`) by using the `find_by` method of the `User` class. For example:

```rb
user = User.find_by(email: 'genevieve@becquerel.me')
```

Typing the variable `user` at the prompt will render the user's Active Record entry, as seen below:

![](/assets/img/admin/user_preview.png)

As you can see in this case, the boolean flag for `admin` is set to `false`, we'll set this to `true` by typing the two following commands, which both switch the boolean to `true` but will commit changes to the database.

```rb
user.admin = true
user.save!
```

![](/assets/img/admin/user_save.png)

## Revoke admin privileges

Perform the same actions as previous but substitute `true` for `false` in the `user.admin = true` line.