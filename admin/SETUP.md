# Admin setup (one time)
1. Open https://enkier.github.io/districtx-legal/admin/ and request a sign-in link to your e-mail; open it.
2. In Supabase → SQL Editor run (replace the e-mail if needed):

    update public.profiles set is_admin = true
    where id = (select id from auth.users where lower(email) = 'x_apps@icloud.com');

3. Reload the admin panel.
