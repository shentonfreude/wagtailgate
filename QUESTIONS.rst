===========
 QUESTIONS
===========

In the tutorial, why is the image gallery a content type under Blog
"app"? Shouldn't it be a content type that's available to any other
content type, e.g., Blog, NewsArticle, Profile, ...?

How to export as a static site, e.g., to S3?

* medusa doesn't support Django > 1.8
* mudusa fork
* wagtail bakery

How to store uploaded media on external server, e.g., S3? Locations:
`media/original_images`, `media/documents/`.

Note that uploaded media is used to generate various sizes in
`media/images/`.

How to store static media on external server? Is this useful?

How to connect to external DB, e.g., PostgreSQL? Presumably standard Django.

How to do nested tags (user created) or categories (admin controlled vocabulary)?


How can we do redirects, after migrating an old site into wagtail?
looks like `wagtailredirects` is the answer.

Search integration with Elasticsearch, especially one running remotely
in the cloud? If Elasticsearch isn't provided, wagtail uses Django ORM search.

508 features for (say) image ALT or LONGDESC tags?

How are navbars (e.g. child pages) implemented -- snippets?
