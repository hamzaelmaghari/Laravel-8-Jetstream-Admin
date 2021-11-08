# Laravel 8 with Jetstream Admin Auth
> Files changed
- routes/web.php
- Database/migrations/2014_10_12_000000_create_users_table.php
- app/Http/Kernel.php

> Files created
- app/Http/Middleware/admin.php
- resources/views/admin/welcome.blade.php

In order to make a user as admin, Go to database manager and check the user **role** and make it **1**.
*0* means simple user.
*1* means admin user (Can access to admin dashboard).

User admin check in blade files:
`
if (Auth::user()->role === 1){
  // Admin content
} else {
  // Not admin content
}
`
**Lets revert that**
`
if (Auth::user()->role === 0){
  // Not admin content
} else {
  // Admin content
}
`
Enjoy :)
