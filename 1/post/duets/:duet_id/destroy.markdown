---
layout: default
title: POST duets/:duet_id/destroy
---
# `{{page.title}}`

Destroy a duet.  A duet can only be destroyed if one of the two following scenarios has occurred:

<ul class="text">
  <li>A duet you proposed has been declined.</li>
  <li>An active duet you're participating in has been canceled by the other person involved.</li>
</ul>

This method should be called after the user has viewed the declined or canceled views.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/destroy`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Response

### `200 OK`

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
