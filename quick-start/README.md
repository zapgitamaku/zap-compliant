---
description: >-
  This page is intended for developers who are new to the platform and want to
  quickly understand how to interact with the API.
---

# Quick Start

{% hint style="info" %}
**Good to know:** The API will return specific error codes and messages in case of an error, developers should be prepared to handle these errors in their applications.
{% endhint %}

## Get your API keys

Your API requests are authenticated using API keys. Any request that doesn't include an API key will return an error.

You can generate an API key from your Dashboard at any time.

{% hint style="info" %}
**Good to know:**

&#x20;Zap production environment- https://api.zap.africa

Zap development environment- https://test-api.zap.africa

Zap waitlist environment- [https://zaplist-server.herokuapp.com/](https://zaplist-server.herokuapp.com/)


{% endhint %}

## Make your first request

To make your first request, send an authenticated request to the users endpoint. This will create a `user`, which is nice.

{% swagger baseUrl="https://test-api.zap.africa/v1" method="post" path="/users" summary="Create new user." %}
{% swagger-description %}
Creates a new user.
{% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %}
The name of the user
{% endswagger-parameter %}

{% swagger-parameter in="body" name="email address" required="true" type="string" %}
The email address of the user
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" type="string" %}
The password of the user
{% endswagger-parameter %}

{% swagger-response status="200" description="User successfully created" %}
```javascript
{
    "name"="Wilson",
    "owner": {
        "id": "sha7891bikojbkreuy",
        "name": "Samuel Passet",
    "species": "Dog",}
    "breed": "Golden Retriever",
}
```
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Good to know:** You can use the API Method block to fully document an API method. You can also sync your API blocks with an OpenAPI file or URL to auto-populate them.
{% endhint %}

