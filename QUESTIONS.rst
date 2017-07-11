===========
 QUESTIONS
===========

In the tutorial, why is the image gallery a content type under Blog
"app"? Shouldn't it be a content type that's available to any other
content type, e.g., Blog, NewsArticle, Profile, ...?

Static Site Export
==================

How to export as a static site, e.g., to S3?

* medusa doesn't support Django > 1.8
* mudusa fork
* wagtail bakery

I tried wagtail-bakery
https://github.com/moorinteractive/wagtail-bakery
and it kinda works but I don't get all my images.

On one page, two of the images show up::

  "GET /media/images/Tamarit_167_Cuina_for_Mimouca_Shen.2e16d0ba.fill-320x240.png HTTP/1.1" 200 60329
  "GET /media/images/P0905_Mercat-Sant-Antoni-4.2e16d0ba.fill-320x240.jpg HTTP/1.1" 200 20274

But not the third:

  Not Found: /media/images/cloudcraft_-_IAF.gov.8e047546.fill-320x240.png
  "GET /media/images/cloudcraft_-_IAF.gov.8e047546.fill-320x240.png HTTP/1.1" 404 1894

Under the build directly media/images we have one with a different
number in the middle, "2e16d0ba" instead of the desired "8e047546"::

  cloudcraft_-_IAF.gov.2e16d0ba.fill-320x240.png

why?

Storing uplodaed media and statics to S3
========================================

How to store uploaded media on external server, e.g., S3? Locations:
`media/original_images`, `media/documents/`.

Note that uploaded media is used to generate various sizes in
`media/images/`.

How to store static media on external server? Is this useful?


Moar
====

How to connect to external DB, e.g., PostgreSQL? Presumably standard Django.

How to do nested tags (user created) or categories (admin controlled vocabulary)?


How can we do redirects, after migrating an old site into wagtail?
looks like `wagtailredirects` is the answer.

Search integration with Elasticsearch, especially one running remotely
in the cloud? If Elasticsearch isn't provided, wagtail uses Django ORM search.

508 features for (say) image ALT or LONGDESC tags?

How are navbars (e.g. child pages) implemented -- snippets?
