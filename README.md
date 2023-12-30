# django-livekit

`livekit` is a Django app to manage livekit conference rooms.

Detailed documentation is in the "docs" directory.

Quick start
-----------

1. Add "livekit" to your INSTALLED_APPS setting like this:

```
    INSTALLED_APPS = [
        ...,
        "livekit",
    ]
```

2. Configure livekit info. You can use `django-environ`:

```
LIVEKIT_API_KEY=deadbeef
LIVEKIT_API_SECRET=secret
LIVEKIT_INSTANCE=meet-asdf.livekit.cloud
```

2. Include the polls URLconf in your project urls.py like this::

    path("livekit/", include("livekit.urls")),

3. Run ``python manage.py migrate`` to create the livekit models.

4. Start the development server and visit http://127.0.0.1:8000/admin/
   to create a room (you'll need the Admin app enabled).

5. Visit http://127.0.0.1:8000/rooms/ to participate in an existing conference room.

